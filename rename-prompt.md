You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/6d95c421cfdc25743ca3bee482775041.css",
    "context": {
      "path": "css/6d95c421cfdc25743ca3bee482775041.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css",
    "context": {
      "path": "css/ed27e4a25bc4107fc0b8184ef8cf6a33.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/072d8d6d99508fb4afc80e33331fc9f3.webp",
    "context": {
      "refs": [
        {
          "alt": "Healthcare & Medical Data Services We have the list of Medical & Healthcare Professional profiles an",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c6cd3e69131c1828fbbdcea1e653a2e.webp",
    "context": {
      "refs": [
        {
          "alt": "FOOD & BEVAREGES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32aa58390ba11605c0bf927d4cdeb142.webp",
    "context": {
      "refs": [
        {
          "alt": "IT SECTOR",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/33c3e502095c5a85d1fb4f3c07c69a80.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Entry Discover the difference a team of experienced data entry operators can make in the way yo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3cab543846ff1d7cff29886e3ef85ea5.webp",
    "context": {
      "refs": [
        {
          "alt": "Market Services Our database experts, skilled with the various nuances of international contact data",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e8bb182a6311d7dbda83641a070a623.webp",
    "context": {
      "refs": [
        {
          "alt": "PHARAMACEUTICAL & NUTRACEUTICAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/519d2ac82daf464fdb1819983d02de7c.webp",
    "context": {
      "refs": [
        {
          "alt": "PROCUREMENT & SUPPLY CHAIN LOGISTICS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/64b075a6e04d3bd3cd70215bd7e1c15d.webp",
    "context": {
      "refs": [
        {
          "alt": "REAL ESTATE & PROPERTY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6cefa52ba84096ea9ea1cd2b2d7e29f7.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Services Data is a critical asset. Placing priorities on attention to detail, quality and perfo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7454e08465b0a538559e758805e8ae24.webp",
    "context": {
      "refs": [
        {
          "alt": "EVENT & MEDIA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75bb5a9de7af5eb4d17831330bcb7213.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/800d356605b116cdfe74b45d8b66f118.webp",
    "context": {
      "refs": [
        {
          "alt": "ENERGY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9150660e1392cecf012f5ae4e20ee1c1.webp",
    "context": {
      "refs": [
        {
          "alt": "HEALTHCARE & MEDICAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a84aac12c69acde05b375ec40964dc02.webp",
    "context": {
      "refs": [
        {
          "alt": "BANKING & FINANCIAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c38e4db4cd890e7122e7d5dd9c424c70.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c70453af3e838fda6336c73ef2113785.webp",
    "context": {
      "refs": [
        {
          "alt": "Data Intelligence Convert data to business, We empower you with the most reliable data metrics and K",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e15a20622104b535a7930bc626f06a32.webp",
    "context": {
      "refs": [
        {
          "alt": "RETAIL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e68631b954563a1291a522a452921371.webp",
    "context": {
      "refs": [
        {
          "alt": "Education",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f1a130035ed1c7593b3246671a1dee54.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f8632a82f5d6c385095a863f7c45da49.webp",
    "context": {
      "refs": [
        {
          "alt": "Event Services We help Event companies to generate new Data & update their existing list, we provide",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Netdata Research Services | Home",
      "first_heading": "Netdata Research Services"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.