# Bobby's Personal Job Board - Weekly Update System

## 🎯 Overview

This document provides a systematic approach for weekly job board updates, ensuring Bobby always has the most current remote physician opportunities tailored to his experience level and preferences.

## 📅 Update Schedule

- **Primary Update Day:** Wednesdays
- **Update Frequency:** Every 7 days
- **Next Update:** September 4, 2025
- **Emergency Updates:** As needed for urgent opportunities

## 🔍 Research Process

### Step 1: Search Major Job Boards
Search the following platforms weekly using these specific queries:

#### Indeed.com
- `"remote physician" "medical director"` 
- `"telemedicine physician" "telehealth"`
- `"utilization review physician" "remote"`
- `"IME physician" "independent medical examiner"`
- `"medical advisor" "remote" "pharmaceutical"`

#### ZipRecruiter.com
- `"Remote Physical Medicine Rehabilitation"`
- `"Remote Physician" salary:200000-500000`
- `"Medical Director Remote"`

#### Glassdoor.com
- `"remote physician jobs"`
- `"medical director" remote`
- `"physician advisor" remote`

#### Specialized Platforms
- **DocCafe.com:** Search "telemedicine" specialty
- **FlexJobs.com:** Medical/healthcare remote jobs
- **PracticeMatch.com:** Remote and telehealth positions

### Step 2: Company Direct Searches
Check career pages monthly:
- **UnitedHealth Group:** careers.unitedhealthgroup.com
- **CVS Health:** jobs.cvshealth.com
- **Teladoc Health:** teladochealth.com/careers
- **CorroHealth:** corrohealth.com/careers
- **Major Insurance Companies:** Anthem, Humana, Kaiser

## ✅ Job Evaluation Criteria

Before adding a job to Bobby's board, ensure it meets these criteria:

### Must-Have Requirements ✅
- [ ] Remote work option (100% or hybrid acceptable)
- [ ] Suitable for 20+ years experience level
- [ ] Board certification required (any specialty acceptable)
- [ ] Low-stress environment or flexible schedule
- [ ] Compensation: $70K+ annually OR $100+ hourly

### Ideal Characteristics ⭐
- [ ] PM&R/Spine expertise valued
- [ ] EMG knowledge applicable
- [ ] Non-clinical or reduced clinical burden
- [ ] Flexible schedule/part-time options
- [ ] No nights/weekends/call requirements

## 📝 Adding New Jobs

### HTML Structure for New Jobs
```html
<div class="job-card">
    <div class="job-header">
        <div class="job-title">[JOB TITLE] <span class="job-status new">NEW</span></div>
        <div class="salary">[SALARY RANGE]</div>
    </div>
    <div class="company">[COMPANY NAME]</div>
    <div class="job-details">
        <div class="detail-row">📍 [LOCATION]</div>
        <div class="detail-row">⏰ [SCHEDULE]</div>
        <div class="detail-row">💻 <span class="remote-badge fully-remote">100% Remote</span></div>
    </div>
    
    <div class="job-description">
        <h4>🎯 Role Overview</h4>
        <p>[DETAILED DESCRIPTION]</p>
        
        <h4>💰 Compensation & Benefits</h4>
        <ul>
            <li>[PAY DETAILS]</li>
            <li>[BENEFITS]</li>
        </ul>
        
        <h4>📋 Key Responsibilities</h4>
        <ul>
            <li>[RESPONSIBILITY 1]</li>
            <li>[RESPONSIBILITY 2]</li>
        </ul>
        
        <div class="benefits-highlight">
            <strong>🌟 Perfect for:</strong> [WHY GOOD FOR BOBBY]
        </div>
    </div>
    
    <div class="requirements">
        <h4>Required Qualifications:</h4>
        <ul>
            <li>[REQUIREMENT 1]</li>
            <li>[REQUIREMENT 2]</li>
        </ul>
    </div>
    
    <div class="contact-info">
        <strong>Contact Information:</strong>
        <div>[CONTACT DETAILS]</div>
    </div>
    
    <a href="[APPLICATION_LINK]" target="_blank" class="apply-link primary">📧 Apply Now</a>
    <a href="[BACKUP_LINK]" target="_blank" class="apply-link">🔍 More Info</a>
</div>
```

## 🏷️ Status Management

### Job Status Tags
- `<span class="job-status new">NEW</span>` - Added within last 7 days
- `<span class="job-status hot">URGENT</span>` - Time-sensitive applications
- `<span class="job-status expired">EXPIRED</span>` - Position filled or expired

### Weekly Status Updates
1. **Remove "NEW" tags** from jobs older than 7 days
2. **Add "EXPIRED" tags** to filled positions
3. **Mark urgent positions** with "HOT" status
4. **Update application deadlines** in job descriptions

## 📊 Statistics Management

The job board automatically counts positions, but verify these manually:

```javascript
// Auto-updating counters in HTML
<div class="stat-number" id="job-count">[AUTO]</div>  // Total active jobs
<div class="stat-number" id="new-count">[AUTO]</div>  // New jobs this week
```

Update these manually if needed:
- **Salary Range:** Check min/max across all positions
- **Remote Percentage:** Calculate % of remote vs hybrid/onsite jobs

## 🔄 Weekly Update Process

### Wednesday Update Checklist

#### Research Phase (30-45 minutes)
- [ ] Search all major job boards using specific queries
- [ ] Check company career pages for direct postings
- [ ] Review medical recruiting firm websites
- [ ] Note any interesting new opportunities

#### Preference Management Phase (15 minutes)
- [ ] **Check Bobby's preferences** using browser console: `getPreferences()`
- [ ] **Remove "not interested" jobs** that are older than a week
- [ ] **Move "interested" jobs** to priority positions (just below NEW jobs)
- [ ] **Note job preferences** for targeted searching

#### Content Update Phase (45-60 minutes)
- [ ] Add 3-5 new high-quality job postings
- [ ] **Prioritize job types** Bobby has marked as "interested"
- [ ] Update existing job descriptions if needed
- [ ] Remove expired/filled positions
- [ ] Update status tags (NEW, HOT, EXPIRED)

#### Technical Update Phase (20 minutes)
- [ ] **Add interest buttons** to all new job postings:
```html
<div class="interest-buttons">
    <button class="interest-btn neutral" onclick="markInterest(this, 'interested')" data-job-id="unique-job-id">
        ⭐ Interested
    </button>
    <button class="interest-btn neutral" onclick="markInterest(this, 'not-interested')" data-job-id="unique-job-id">
        ❌ Not Interested
    </button>
</div>
```
- [ ] Update the "Last Updated" date in header
- [ ] Update "Next Update" date in footer
- [ ] Verify job counter accuracy (excludes not-interested jobs)
- [ ] Update the update log with changes made

#### Final Review Phase (15 minutes)
- [ ] Test application links
- [ ] Test interest tracking buttons
- [ ] Verify contact information
- [ ] Check mobile responsiveness
- [ ] Proofread new content

## 📋 Update Log Template

```html
<div class="update-log">
    <h3>📅 Weekly Update Log - [DATE]</h3>
    <ul>
        <li class="added">Added [#] new [type] positions: [company names]</li>
        <li class="updated">Updated [position] with [changes]</li>
        <li class="expired">Removed [#] expired positions</li>
        <li class="added">Research shows [current market insight]</li>
    </ul>
</div>
```

## 🚨 Priority Search Terms

These search terms typically yield high-value opportunities:
- **"Part-time Medical Director"** - Often offers excellent work-life balance
- **"Independent Medical Examiner"** - Frequently provides high hourly rates
- **"Physician Advisor" OR "Medical Advisor"** - Usually consultative in nature
- **"Utilization Review Physician"** - Common at insurance companies
- **"Telemedicine Physician MSK" OR "Telehealth Spine"** - Good specialty alignment
- **"Medical Science Liaison Spine"** - Available in pharmaceutical companies
- **"Expert Witness Medical"** - Often provides premium hourly compensation
- **"Remote Medical Writing"** - Typically offers flexible, intellectual work

## 📈 Success Metrics

Track these KPIs weekly:
- **Total Active Jobs:** Target 30-40 positions
- **New Jobs Added:** Target 3-5 per week
- **Application Response Rate:** Monitor which positions get responses
- **Salary Range Expansion:** Track improvements in compensation offerings
- **Remote Percentage:** Maintain 85%+ remote opportunities

## 🔗 Quick Reference Links

### Job Boards
- [Indeed Remote Physician Jobs](https://www.indeed.com/q-remote-physician-jobs.html)
- [ZipRecruiter Remote PM&R](https://www.ziprecruiter.com/Jobs/Remote-Physical-Medicine-And-Rehabilitation-Physician)
- [Glassdoor Remote Physician](https://www.glassdoor.com/Job/remote-physician-jobs-SRCH_IL.0,6_IS11047_KO7,16.htm)
- [DocCafe Telemedicine](https://www.doccafe.com/physician-jobs/specialty/telemedicine)

### Company Career Pages
- [UnitedHealth Careers](https://careers.unitedhealthgroup.com)
- [CVS Health Jobs](https://jobs.cvshealth.com)
- [Teladoc Careers](https://www.teladochealth.com/careers)
- [FlexJobs Medical](https://www.flexjobs.com/remote-jobs/medical)

## 💡 Pro Tips

1. **Best Search Times:** Tuesday-Thursday mornings for freshest postings
2. **Save Searches:** Set up alerts on major job boards
3. **Network Leverage:** Check LinkedIn for connections at target companies
4. **Application Timing:** Apply within 24-48 hours of job posting
5. **Follow-up Strategy:** Contact recruiters directly when possible

---

*This system ensures Bobby's job board remains current, comprehensive, and focused on the best remote opportunities for experienced physiatrists.*