<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Master Presentations & Designs</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: linear-gradient(to bottom, #f0f8ff, #e6e6fa); color: #333; }
        header { background: #4a90e2; color: white; padding: 20px; text-align: center; }
        nav { background: #333; padding: 10px; text-align: center; }
        nav a { color: white; margin: 0 15px; text-decoration: none; }
        section { padding: 20px; max-width: 800px; margin: 0 auto; }
        .tip { background: #fff; border-left: 5px solid #4a90e2; padding: 10px; margin: 10px 0; }
        .interactive { background: #f9f9f9; padding: 20px; border-radius: 8px; margin: 20px 0; }
        button { background: #4a90e2; color: white; border: none; padding: 10px; cursor: pointer; }
        input, textarea { width: 100%; padding: 10px; margin: 10px 0; }
        footer { background: #333; color: white; text-align: center; padding: 10px; }
        @media (max-width: 600px) { nav a { display: block; margin: 5px 0; } }
    </style>
</head>
<body>
    <header>
        <h1>Master Presentations & Designs</h1>
        <p>Learn to create catchy, professional presentations and designs that wow your audience.</p>
    </header>
    <nav>
        <a href="#tips">Tips</a>
        <a href="#examples">Examples</a>
        <a href="#tools">Tools</a>
        <a href="#interactive">Build Your Own</a>
    </nav>
    
    <section id="tips">
        <h2>Essential Tips for Catchy Presentations</h2>
        <div class="tip">
            <h3>1. Start with a Strong Hook</h3>
            <p>Use a surprising fact, question, or visual to grab attention. For example, "Did you know 90% of presentations fail due to poor design?"</p>
        </div>
        <div class="tip">
            <h3>2. Keep It Visual</h3>
            <p>Incorporate high-quality images, infographics, and minimal text. Tools like Canva make this easy.</p>
        </div>
        <div class="tip">
            <h3>3. Use Color Wisely</h3>
            <p>Choose a color scheme that matches your brand. Blue for trust, red for energy—avoid clashing combos.</p>
        </div>
        <div class="tip">
            <h3>4. Practice Delivery</h3>
            <p>Rehearse timing and body language. Record yourself to spot improvements.</p>
        </div>
    </section>
    
    <section id="examples">
        <h2>Examples of Great Designs</h2>
        <p>Here are templates and ideas:</p>
        <ul>
            <li><strong>Minimalist Slide:</strong> White background, bold headline, one key image. Ideal for tech talks.</li>
            <li><strong>Storytelling Layout:</strong> Use timelines or flowcharts to guide the narrative.</li>
            <li><strong>Interactive Infographic:</strong> Embed clickable elements in tools like Prezi.</li>
        </ul>
        <p>Download free templates from sites like SlideShare or Canva.</p>
    </section>
    
    <section id="tools">
        <h2>Recommended Tools</h2>
        <ul>
            <li><strong>PowerPoint/Google Slides:</strong> Free, versatile for beginners.</li>
            <li><strong>Canva:</strong> Drag-and-drop design with templates.</li>
            <li><strong>Keynote:</strong> Mac-exclusive, great for animations.</li>
            <li><strong>Adobe Spark:</strong> For social media graphics.</li>
        </ul>
    </section>
    
    <section id="interactive">
        <h2>Build Your Own Presentation</h2>
        <p>Use this simple tool to create and preview slides.</p>
        <input type="text" id="slideTitle" placeholder="Enter slide title">
        <textarea id="slideContent" placeholder="Enter slide content"></textarea>
        <button onclick="addSlide()">Add Slide</button>
        <button onclick="previewPresentation()">Preview Presentation</button>
        <div id="slides"></div>
        <div id="preview" style="display:none; background:white; padding:20px; border:1px solid #ccc;"></div>
    </section>
    
    <footer>
        <p>&copy; 2023 Master Presentations. Built with love for educators.</p>
    </footer>
    
    <script>
        let slides = [];
        function addSlide() {
            const title = document.getElementById('slideTitle').value;
            const content = document.getElementById('slideContent').value;
            if (title && content) {
                slides.push({ title, content });
                document.getElementById('slides').innerHTML += `<p>Slide ${slides.length}: ${title}</p>`;
                document.getElementById('slideTitle').value = '';
                document.getElementById('slideContent').value = '';
            }
        }
        function previewPresentation() {
            const preview = document.getElementById('preview');
            preview.innerHTML = slides.map((slide, index) => `<div><h3>Slide ${index+1}: ${slide.title}</h3><p>${slide.content}</p></div>`).join('');
            preview.style.display = 'block';
        }
    </script>
</body>
</html>
