import { Facebook, Instagram, Twitter, Phone } from "lucide-react";

export default function WeWorkWebsite() {
  const services = [
    { title: "Barista Services", image: "https://source.unsplash.com/featured/?coffee,barista" },
    { title: "Craft Making", image: "https://source.unsplash.com/featured/?african,crafts" },
    { title: "Bamboo Carpentry", image: "https://source.unsplash.com/featured/?bamboo,carpentry" },
    { title: "Tour Guiding", image: "https://source.unsplash.com/featured/?uganda,tourism" },
    { title: "Solar Installation", image: "https://source.unsplash.com/featured/?solar,energy" },
  ];

  const posts = [
    { title: "Behind the scenes: Building eco-friendly furniture", tag: "#Carpentry", img: "https://source.unsplash.com/featured/?woodworking,uganda" },
    { title: "Meet Jane, our first female solar installer!", tag: "#SolarEnergy", img: "https://source.unsplash.com/featured/?female,solar" },
  ];

  return (
    <div className="p-6 space-y-6 bg-white text-gray-800">
      <header className="text-center space-y-3">
        <h1 className="text-4xl font-bold text-green-700">WeWork Uganda Youth Services</h1>
        <p className="text-lg text-gray-600">Empowering youth through green and decent jobs</p>
        <div className="flex justify-center space-x-4">
          <button className="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded">Book a Service</button>
          <button className="border px-4 py-2 rounded border-green-600 text-green-600">Shop Crafts</button>
        </div>
      </header>

      <section className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        {services.map((trade) => (
          <div key={trade.title} className="rounded-lg shadow-md overflow-hidden">
            <img src={trade.image} alt={trade.title} className="w-full h-40 object-cover" />
            <div className="p-4 space-y-2">
              <h3 className="text-xl font-semibold">{trade.title}</h3>
              <p className="text-sm text-gray-500">Professional, youth-led services in {trade.title.toLowerCase()}.</p>
              <div className="flex flex-wrap gap-2 text-xs text-green-600">
                <span>#YouthEmpowerment</span>
                <span>#{trade.title.replace(/\\s+/g, '')}</span>
                <span>#MadeInUganda</span>
              </div>
              <button className="w-full mt-2 bg-green-600 hover:bg-green-700 text-white py-2 rounded">Contact Now</button>
            </div>
          </div>
        ))}
      </section>

      <section className="mt-8 space-y-4">
        <h2 className="text-2xl font-bold text-green-700">Latest Posts</h2>
        {posts.map((post, idx) => (
          <div key={idx} className="flex gap-4 items-start">
            <img src={post.img} alt={post.title} className="w-32 h-24 rounded object-cover" />
            <div>
              <h3 className="text-md font-semibold">{post.title}</h3>
              <p className="text-sm text-gray-500">{post.tag}</p>
            </div>
          </div>
        ))}
      </section>

      <footer className="pt-6 border-t mt-6 text-center space-y-3">
        <p>Contact us: +256 787 701 359 | +256 703 123 456</p>
        <div className="flex justify-center space-x-4">
          <a href="https://facebook.com/weworkug" target="_blank" rel="noopener noreferrer"><Facebook /></a>
          <a href="https://instagram.com/weworkug" target="_blank" rel="noopener noreferrer"><Instagram /></a>
          <a href="https://twitter.com/weworkug" target="_blank" rel="noopener noreferrer"><Twitter /></a>
          <a href="tel:+256787701359"><Phone /></a>
        </div>
        <p className="text-sm text-gray-400">Page Visits: 1,234 | Referrals: Facebook (45%), Instagram (30%), Direct (25%)</p>
      </footer>
    </div>
  );
}
