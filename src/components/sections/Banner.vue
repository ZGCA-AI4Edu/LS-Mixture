<template>
    <div class="banner-container">
      <h1 class="title">
        Long-Short Chain-of-Thought Mixture Supervised Fine-Tuning Eliciting Efficient Reasoning in Large Language Models
      </h1>
      <h2 class="subtitle">
        we propse a new method: <span class="highlight font-bold">LS-Mixture SFT</span>
      </h2>
  
      <div>
        <img src="/arch.svg" alt="LS-Mixture SFT Architecture" />
      </div>
  
      <div class="results-container">
        <div class="result-box">
          <span class="result-value text-green-400">+2.3%</span>
          <span class="result-label">Average Accuracy Improvement</span>
        </div>
        <div class="result-box">
          <span class="result-value text-green-400">-47.61%</span>
          <span class="result-label">Reduction in Response Length</span>
        </div>
      </div>
  
      <p class="text-xs mt-6 opacity-70">
        Enabling efficient reasoning while avoiding overthinking.
      </p>
    </div>
  </template>
  
  <script setup>
  // 组件逻辑（如果需要）
  </script>
  
  <style scoped>
  .banner-container {
    width: 100%;
    max-width: 900px;
    background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    border-radius: 1rem;
    padding: 2rem;
    box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
    text-align: center;
    margin: 2rem auto;
  }
  
  /* 其他样式保持不变，从banner.html复制过来 */
  .title {
    font-size: 1.75rem;
    font-weight: 900;
    line-height: 1.3;
    margin-bottom: 1rem;
  }
  
  .subtitle {
    font-size: 1.1rem;
    font-weight: 600;
    color: #ede9fe;
    margin-bottom: 1.5rem;
  }
  
  .highlight {
    background-color: rgba(255, 255, 255, 0.2);
    padding: 0.1rem 0.5rem;
    border-radius: 0.375rem;
  }
  
  .reasoning-path-container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin: 2rem 0;
    gap: 1rem;
  }
  
  .path-element {
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 0.75rem;
    padding: 1.5rem;
    flex: 1;
    min-height: 180px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 1px solid rgba(255, 255, 255, 0.3);
  }
  
  .path-label {
    font-size: 0.9rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
    color: #d1d5db;
  }
  
  .arrow {
    font-size: 2.5rem;
    font-weight: bold;
    color: #a78bfa;
    transform: scale(1.5);
  }
  
  .results-container {
    display: flex;
    justify-content: space-around;
    margin-top: 2rem;
    gap: 1rem;
  }
  
  .result-box {
    background-color: rgba(255, 255, 255, 0.15);
    padding: 1rem;
    border-radius: 0.75rem;
    flex-grow: 1;
    border: 1px solid rgba(255, 255, 255, 0.3);
  }
  
  .result-value {
    font-size: 1.5rem;
    font-weight: 700;
    display: block;
    margin-bottom: 0.25rem;
  }
  
  .result-label {
    font-size: 0.8rem;
    color: #e5e7eb;
  }
  
  .chain-viz {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    height: 80px;
  }
  
  .long-chain-viz {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }
  
  .long-chain-segment {
    width: 60px;
    height: 8px;
    background-color: #fde047;
    margin-bottom: 6px;
    border-radius: 4px;
  }
  
  .long-chain-segment:nth-child(2) { width: 45px; margin-left:10px;}
  .long-chain-segment:nth-child(3) { width: 70px; }
  .long-chain-segment:nth-child(4) { width: 50px; margin-left:5px;}
  
  .short-chain-viz {
    width: 80px;
    height: 12px;
    background-color: #86efac;
    border-radius: 6px;
  }
  
  @media (max-width: 768px) {
    .title {
      font-size: 1.5rem;
    }
    .subtitle {
      font-size: 1rem;
    }
    .reasoning-path-container, .results-container {
      flex-direction: column;
      gap: 1.5rem;
    }
    .arrow {
      transform: rotate(90deg) scale(1.2);
      margin: 1rem 0;
    }
    .path-element {
      min-height: 150px;
    }
  }
  
  @media (max-width: 480px) {
    .banner-container {
      padding: 1.5rem;
    }
    .title {
      font-size: 1.25rem;
    }
    .subtitle {
      font-size: 0.9rem;
    }
    .result-value {
      font-size: 1.25rem;
    }
    .long-chain-segment {
      width: 40px;
      height: 6px;
      margin-bottom: 4px;
    }
    .long-chain-segment:nth-child(2) { width: 30px; margin-left:5px;}
    .long-chain-segment:nth-child(3) { width: 50px; }
    .long-chain-segment:nth-child(4) { width: 35px; margin-left:3px;}
  
    .short-chain-viz {
      width: 60px;
      height: 10px;
    }
  }
  </style>