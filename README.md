# my-website
this website is the result of exploration
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  html {
    scroll-behavior: smooth;
  }
  
  body {
    @apply font-sans antialiased;
  }
}

@layer components {
  .line-clamp-2 {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  
  .line-clamp-3 {
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  
  .prose {
    @apply text-gray-800 leading-relaxed;
  }
  
  .prose h1 {
    @apply text-3xl font-bold text-gray-900 mt-8 mb-4;
  }
  
  .prose h2 {
    @apply text-2xl font-bold text-gray-900 mt-6 mb-3;
  }
  
  .prose h3 {
    @apply text-xl font-semibold text-gray-900 mt-5 mb-3;
  }
  
  .prose p {
    @apply mb-4 leading-relaxed;
  }
  
  .prose a {
    @apply text-orange-600 hover:text-orange-700 transition-colors;
  }
  
  .prose ul, .prose ol {
    @apply mb-4 pl-6;
  }
  
  .prose li {
    @apply mb-2;
  }
  
  .prose blockquote {
    @apply border-l-4 border-orange-500 pl-4 py-2 my-6 bg-orange-50 text-gray-800 italic;
  }
  
  .prose code {
    @apply bg-gray-100 text-gray-800 px-2 py-1 rounded text-sm font-mono;
  }
  
  .prose pre {
    @apply bg-gray-900 text-gray-100 p-4 rounded-lg overflow-x-auto my-6;
  }
  
  .prose pre code {
    @apply bg-transparent p-0 text-gray-100;
  }
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  @apply bg-gray-100;
}

::-webkit-scrollbar-thumb {
  @apply bg-gray-400 rounded-full;
}

::-webkit-scrollbar-thumb:hover {
  @apply bg-gray-500;
}

/* Loading animation */
@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }
  100% {
    background-position: 468px 0;
  }
}

.loading-shimmer {
  animation: shimmer 1.2s ease-in-out infinite;
  background: linear-gradient(to right, #f6f7f8 8%, #edeef1 18%, #f6f7f8 33%);
  background-size: 800px 104px;
}

/* Focus styles for accessibility */
*:focus {
  @apply outline-none ring-2 ring-orange-500 ring-offset-2;
}

/* Smooth transitions for all interactive elements */
button, a, input, select, textarea {
  @apply transition-all duration-200;
}
