# 🏨 Hotel Booking Analysis Project

## 📊 Overview
This project presents a comprehensive analysis of hotel booking data across City and Resort hotels, uncovering key drivers of cancellations, revenue patterns, and customer behaviors. With over **119,000 bookings** (reduced to **87,396** after cleaning), the goal is to provide actionable insights to improve hotel operations, revenue management, and guest experience.

---

### 🔍 Comprehensive Insights from Hotel Booking Analysis

---

#### **1. Dataset Overview**
- **Size**: 119,390 rows × 32 columns  
- **Cleaned**: 87,396 rows × 30 columns  
- **Highlights**:
  - `is_canceled`: 37.04% of bookings canceled  
  - `lead_time`: Avg 104 days (Max 737)  
  - `adr`: Avg Daily Rate = €102.01  
  - Data spans **2015 to 2017**

---

#### **2. Data Cleaning & Preprocessing**
- **Duplicates Removed**: 31,994
- **Missing Value Treatment**:
  - `children`: filled with 0
  - `country`: filled with mode (Portugal)
  - `agent`, `company`: filled with 0
- **Type Conversions**:
  - `is_canceled` → boolean  
  - `arrival_date_*` → categorical  
  - Combined into a datetime `arrival_date`

---

#### **3. Key Findings on Cancellations**

##### A. Cancellation Rate by Market Segment
| Market Segment       | Cancellation Rate |
|----------------------|------------------|
| Not Specified        | 100%             |
| Online TA            | 35%              |
| Offline TA/TO        | 27%              |
| Groups               | 20%              |
| Corporate            | 12%              |
| Direct               | 10%              |

🔎 **Insight**: OTAs are most cancellation-prone; direct bookings are the most reliable.

##### B. Lead Time Impact
- Lead time > 300 days → >50% cancellations  
- ADR increases with lead time → early bookings pay more and cancel more

##### C. Deposit Type
| Deposit Type     | Cancellation Rate |
|------------------|------------------|
| Non-Refund       | 94.7%            |
| No Deposit       | 26.7%            |
| Refundable       | 24.3%            |

🔎 **Insight**: Non-refundable policies show highest cancellations — policy mismatch?

##### D. Room Type Mismatch
- When reserved ≠ assigned room:
  - Cancellation rate: 47.1%
  - ADR: €84.14 (below avg)

---

#### **4. Guest Behavior**

##### A. Repeated vs New Guests
| Guest Type     | Cancellation Rate | ADR (€)  |
|----------------|-------------------|----------|
| Repeated Guest | 8%                | 64.59    |
| New Guest      | 28%               | 107.34   |

🔎 **Insight**: Repeated guests cancel 3.5x less and pay less — loyal but lower yield.

##### B. Group Size & Special Requests
- Large groups (5+): ~40% cancellations  
- 0 requests: 33% cancellations  
- 3+ requests: <10% cancellations

##### C. Corporate vs Individual
| Booking Type | Cancellation Rate | ADR (€) |
|--------------|-------------------|--------|
| Corporate    | 14%               | 95.02  |
| Individual   | 29%               | 107.34 |

🔎 **Insight**: Corporate clients are more stable but less profitable per booking

---

#### **5. Seasonal Trends**

##### A. Monthly Cancellations
- Peak: July–August (~32%)
- Low: November (21%)

##### B. ADR by Month
| Month    | ADR (€) | Cancellation Rate |
|----------|---------|-------------------|
| August   | 150.88  | 32%               |
| January  | 70.05   | 22%               |

🔎 **Insight**: High ADR in summer → high cancellations; pricing elasticity?

---

#### **6. Hotel-Type Differences**
| Hotel Type  | Cancellation Rate | ADR (€) |
|-------------|-------------------|--------|
| City Hotel  | Higher            | 120+   |
| Resort Hotel| Lower             | 90–100 |

🔎 **Insight**: City hotels are riskier for revenue forecasting

---

#### **7. Country-Specific Trends**
- **Highest Cancellation Rates**:
  - Brazil (36%), Portugal (35%), Italy (35%)
- **Lowest**: Netherlands (18%), Germany (19%)

---

## ✅ Actionable Recommendations
1. **Reduce OTA reliance**: Promote direct bookings (10% cancellations)
2. **Shorter lead-time incentives**: Reduce cancellations from early planners
3. **Reward loyalty**: Encourage repeat guests
4. **Fix room mismatches**: Can reduce cancellations by ~47%
5. **Revise deposit policies**: Avoid non-refundable-only strategy
6. **Seasonal control**: Stricter rules in July–August

---

## 🛠️ Tools & Tech Used
- **Python Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Analysis Techniques**:
  - Grouping & aggregation
  - Dual-axis plots
  - Time-series analysis
  - Cancellation rate heatmaps

---

## 🏁 Conclusion
Cancellations are influenced by **lead time**, **deposit policies**, **booking channel**, and **room allocation issues**. Targeted interventions across these areas can significantly boost revenue retention and reduce booking uncertainty.

---

## 🚀 Author
**Murtaza Hussain**  
_Data Analyst | Python Enthusiast | Storytelling through Data_  
🔗 GitHub: [github.com/MurtazaHussain72](https://github.com/MurtazaHussain72)

---

## ⭐ If you found this project valuable, please star the repo and connect!
