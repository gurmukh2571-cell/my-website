# my-weimport { motion } from 'framer-motion';
import { Button } from "@/components/ui/button";

export default function HomePage() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Header */}
      <header className="flex justify-between items-center px-10 py-6 shadow-sm bg-white">
        <h1 className="text-2xl font-bold">MyWebsite</h1>
        <nav className="flex gap-6 text-lg">
          <a href="#home" className="hover:text-blue-600">Home</a>
          <a href="#about" className="hover:text-blue-600">About</a>
          <a href="#features" className="hover:text-blue-600">Features</a>
          <a href="#contact" className="hover:text-blue-600">Contact</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section id="home" className="flex flex-col items-center justify-center text-center py-24 px-6 bg-gradient-to-r from-blue-500 to-indigo-600 text-white">
        <motion.h2 initial={{ opacity: 0, y: -30 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.7 }} className="text-5xl font-extrabold mb-4">
          Welcome to MyWebsite
        </motion.h2>
        <motion.p initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.4 }} className="text-lg max-w-2xl mb-8">
          A modern, responsive, and simple website built using React, Tailwind, and Framer Motion.
        </motion.p>
        <Button className="bg-white text-blue-600 hover:bg-gray-200">Get Started</Button>
      </section>

      {/* About Section */}
      <section id="about" className="py-20 px-10 bg-white">
        <h3 className="text-3xl font-bold mb-4 text-center">About Us</h3>
        <p className="text-center max-w-3xl mx-auto text-gray-600">
          We build modern, clean, and interactive websites for personal, educational, and business use. Our mission is to make web design simple for everyone.
        </p>
      </section>

      {/* Features Section */}
      <section id="features" className="py-20 px-10 bg-gray-100">
        <h3 className="text-3xl font-bold mb-12 text-center">Features</h3>
        <div className="grid md:grid-cols-3 gap-8">
          {[
            { title: 'Fast Performance', desc: 'Optimized for speed and smooth browsing experience.' },
            { title: 'Responsive Design', desc: 'Looks great on desktop, tablet, and mobile.' },
            { title: 'Easy Customization', desc: 'Easily edit content and style with simple tools.' }
          ].map((feature, i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.05 }}
              className="bg-white p-6 rounded-2xl shadow text-center"
            >
              <h4 className="text-xl font-semibold mb-2">{feature.title}</h4>
              <p className="text-gray-600">{feature.desc}</p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-20 px-10 bg-white text-center">
        <h3 className="text-3xl font-bold mb-6">Contact Us</h3>
        <p className="max-w-2xl mx-auto text-gray-600 mb-8">
          Have any questions or ideas? Feel free to reach out and let’s create something amazing together!
        </p>
        <Button className="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 text-lg rounded-xl">Send Message</Button>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-gray-400 py-6 text-center">
        <p>© {new Date().getFullYear()} MyWebsite. All rights reserved.</p>
      </footer>
    </div>
  );
}
bsite
