# ⚡ LogistIQ Pro - Quick Start Guide

## 🎯 Get Running in 5 Minutes

### Step 1: Install Dependencies (2 minutes)

```bash
cd logistiq-pro

# Install all requirements
pip install -r requirements.txt
```

**Note:** If `pip install` fails for some packages, install minimum required:
```bash
pip install google-generativeai streamlit plotly pandas python-dotenv
```

---

### Step 2: Set Up API Key (1 minute)

1. Get Google API Key (free):
   - Go to: https://makersuite.google.com/app/apikey
   - Click "Create API Key"
   - Copy the key

2. Create `.env` file:
```bash
cp .env.example .env
```

3. Edit `.env` and add your key:
```
GOOGLE_API_KEY=your_key_here
```

---

### Step 3: Run Demo (2 minutes)

```bash
python demos/main_demo.py
```

You'll see:
- ✅ SlotIQ Agent optimizing bookings
- 🚨 Urgent order handling in 8 seconds
- ⚠️ Multi-crisis coordination

**Press Enter to advance through demos**

---

### Optional: Run Dashboard

```bash
streamlit run app/dashboard.py
```

Opens browser at http://localhost:8501

---

## 🎬 What to Show in Demo

### For Judges/Reviewers:

1. **Architecture** - Show README.md diagrams
2. **Working Code** - Run `python demos/main_demo.py`
3. **Agent Logic** - Open `src/agents/slot_agent.py` (complete implementation)
4. **Dashboard** - Run `streamlit run app/dashboard.py`

---

## 📁 Key Files to Highlight

### Complete Implementations:
- `src/agents/slot_agent.py` - **FULLY WORKING SlotIQ Agent**
- `src/agents/orchestrator.py` - Multi-agent coordination
- `src/data/mock_data_generator.py` - Realistic data
- `demos/main_demo.py` - Live demonstrations

### Architecture Documentation:
- `README.md` - Complete system overview
- `src/database/db_manager.py` - State management
- `app/dashboard.py` - Monitoring interface

### Skeleton for Extension:
- `src/agents/load_agent.py` - TODO: 3D bin packing
- `src/agents/priority_cost_agents.py` - TODO: Advanced logic

---

## 🐛 Troubleshooting

### "ModuleNotFoundError: No module named 'google.generativeai'"
```bash
pip install google-generativeai
```

### "GOOGLE_API_KEY not found"
- Make sure `.env` file exists in project root
- Check that key is correctly formatted (no quotes, no spaces)

### "ImportError: cannot import name 'SlotIQAgent'"
```bash
# Make sure you're in project root
cd logistiq-pro
python demos/main_demo.py
```

### Dashboard won't start
```bash
pip install streamlit plotly
streamlit run app/dashboard.py
```

---

## 💡 Quick Testing Commands

```bash
# Test SlotIQ Agent directly
python src/agents/slot_agent.py

# Generate mock data
python src/data/mock_data_generator.py

# Run orchestrator demo
python src/agents/orchestrator.py

# Full demo
python demos/main_demo.py
```

---

## 🎯 What Works Right Now

✅ **Fully Functional:**
- SlotIQ Agent (complete with Gemini integration)
- Multi-agent orchestration framework
- Mock data generation
- Database structure
- Dashboard UI
- All demos

⚠️ **Skeleton (TODOs for later):**
- LoadIQ 3D bin packing algorithm
- PriorityIQ ML classification
- CostIQ detailed financial models
- ChromaDB memory integration

**But this is PERFECT for MVP submission!**

---

## 🚀 For Kaggle Submission

1. ✅ Upload code to GitHub
2. ✅ Submit writeup (already done)
3. ✅ Add GitHub link to writeup
4. 📹 *Optional:* Record 3-min demo video

---

## ❓ Need Help?

Check these files:
- `README.md` - Full documentation
- `GITHUB_INSTRUCTIONS.md` - How to upload
- `requirements.txt` - Dependencies list

---

**You're all set! Good luck with the competition!** 🏆
