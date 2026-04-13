<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
  <title>SchemeVault Admin</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { 
      font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; 
      background: #f8fafc; 
      padding: 16px; 
      color: #0f172a; 
      min-height: 100vh;
      overflow-x: hidden;
    }
    .container { max-width: 1440px; margin: 0 auto; width: 100%; overflow-x: hidden; }
    .login-panel { background: white; padding: clamp(24px, 5vw, 40px); border-radius: 28px; max-width: 420px; width: 100%; margin: clamp(60px, 15vh, 120px) auto; box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; }
    .login-panel h2 { margin-bottom: 24px; font-weight: 600; font-size: 1.8rem; }
    .dashboard { display: none; }
    .dashboard-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 28px; flex-wrap: wrap; gap: 16px; }
    .dashboard-header h1 { font-size: clamp(1.8rem, 5vw, 2.2rem); font-weight: 600; }
    .header-actions { display: flex; gap: 10px; flex-wrap: wrap; }
    .logout-btn { background: white; border: 1px solid #e2e8f0; padding: 10px 18px; border-radius: 40px; font-weight: 500; cursor: pointer; transition: all 0.15s; font-size: 0.9rem; }
    .logout-btn:hover { background: #f8fafc; border-color: #cbd5e1; }
    .card-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 20px 0; }
    .card { background: white; border-radius: 24px; padding: clamp(18px, 4vw, 28px); border: 1px solid #e2e8f0; box-shadow: 0 4px 6px -2px rgba(0,0,0,0.02); width: 100%; }
    .card h3 { font-weight: 600; margin-bottom: 20px; padding-bottom: 14px; border-bottom: 1px solid #f1f5f9; font-size: 1.2rem; display: flex; align-items: center; gap: 8px; }
    input, select, textarea { width: 100%; padding: 11px 14px; border: 1.5px solid #e2e8f0; border-radius: 16px; font-size: 0.95rem; background: white; transition: all 0.15s; }
    input:focus, select:focus, textarea:focus { outline: none; border-color: #059669; box-shadow: 0 0 0 4px rgba(5,150,105,0.08); }
    button { background: #059669; color: white; border: none; padding: 11px 22px; border-radius: 40px; font-weight: 500; cursor: pointer; transition: all 0.15s; font-size: 0.95rem; display: inline-flex; align-items: center; justify-content: center; gap: 6px; white-space: nowrap; }
    button:hover { background: #047857; }
    button.secondary { background: white; color: #0f172a; border: 1.5px solid #e2e8f0; }
    button.secondary:hover { background: #f8fafc; }
    button.danger { background: #ef4444; }
    button.danger:hover { background: #dc2626; }
    button.small { padding: 6px 14px; font-size: 0.85rem; }
    .form-group { margin-bottom: 18px; }
    .form-row { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 16px; }
    label { display: block; font-weight: 500; margin-bottom: 6px; color: #334155; font-size: 0.9rem; }
    .schemes-list { display: grid; gap: 12px; max-height: 500px; overflow-y: auto; }
    .scheme-item { display: flex; justify-content: space-between; align-items: flex-start; padding: 16px; background: #fafbfc; border-radius: 18px; border: 1px solid #edf2f7; flex-wrap: wrap; gap: 12px; }
    .scheme-info h4 { font-weight: 600; margin-bottom: 4px; }
    .scheme-info small { color: #64748b; display: block; line-height: 1.5; }
    .scheme-actions { display: flex; gap: 8px; }
    .modal { display: none; position: fixed; inset: 0; background: rgba(15,23,42,0.5); backdrop-filter: blur(6px); align-items: center; justify-content: center; z-index: 1000; padding: 16px; }
    .modal.open { display: flex; }
    .modal-content { background: white; padding: clamp(20px, 5vw, 32px); border-radius: 32px; max-width: 550px; width: 100%; max-height: 85vh; overflow-y: auto; box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25); }
    .status-badge { display: inline-block; padding: 4px 12px; border-radius: 40px; font-size: 0.8rem; font-weight: 500; }
    .status-online { background: #dcfce7; color: #166534; }
    .status-offline { background: #fee2e2; color: #991b1b; }
    .toast { position: fixed; top: 20px; right: 20px; background: white; padding: 14px 22px; border-radius: 40px; box-shadow: 0 15px 30px -10px rgba(0,0,0,0.15); border-left: 5px solid #059669; z-index: 2000; font-weight: 500; max-width: 350px; animation: slideIn 0.2s ease; }
    .toast.error { border-left-color: #ef4444; }
    @keyframes slideIn { from { opacity: 0; transform: translateX(20px); } to { opacity: 1; transform: translateX(0); } }
    .bulk-upload-area { border: 2.5px dashed #cbd5e1; border-radius: 24px; padding: 28px 20px; text-align: center; cursor: pointer; }
    .bulk-upload-area:hover { border-color: #059669; background: #f0fdf4; }
    .tabs { display: flex; gap: 4px; margin: 24px 0 20px; border-bottom: 1.5px solid #e2e8f0; flex-wrap: wrap; overflow-x: auto; scrollbar-width: none; }
    .tabs::-webkit-scrollbar { display: none; }
    .tab { padding: 12px 22px; cursor: pointer; border: none; background: none; color: #64748b; font-weight: 500; font-size: 0.95rem; white-space: nowrap; border-radius: 40px 40px 0 0; }
    .tab.active { color: #059669; border-bottom: 3px solid #059669; }
    .tab-content { display: none; }
    .tab-content.active { display: block; }
    .visitor-log { max-height: 220px; overflow-y: auto; font-size: 0.85rem; background: #fafbfc; border-radius: 16px; padding: 8px 4px; }
    .visitor-log div { padding: 8px 12px; border-bottom: 1px solid #edf2f7; }
    .stats-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 16px; }
    .stat-item { background: #f8fafc; padding: 14px 12px; border-radius: 18px; text-align: center; }
    .stat-value { font-size: 2rem; font-weight: 700; color: #059669; }
    .stat-label { color: #64748b; font-size: 0.8rem; text-transform: uppercase; }
    .progress-container { margin: 12px 0; }
    .progress-bar-wrapper { display: flex; align-items: center; gap: 12px; }
    progress { flex: 1; height: 10px; border-radius: 10px; }
    progress::-webkit-progress-bar { background: #e2e8f0; border-radius: 10px; }
    progress::-webkit-progress-value { background: #059669; border-radius: 10px; }
    .progress-percent { min-width: 45px; font-weight: 600; color: #059669; }
    @media (max-width: 640px) {
      .card-grid { grid-template-columns: 1fr; }
      button { width: 100%; }
      .header-actions button { width: auto; }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Login Panel -->
    <div id="loginPanel" class="login-panel">
      <h2>Admin Access</h2>
      <div style="margin-bottom:24px"><span id="connectionStatus" class="status-badge status-offline">Checking connection</span></div>
      <div class="form-group"><label>Password</label><input type="password" id="adminPassword" placeholder="Enter admin password"></div>
      <button id="loginBtn" style="width:100%">Sign In</button>
      <p id="loginError" style="color:#dc2626; margin-top:14px;"></p>
      <button id="retryConnectionBtn" class="secondary" style="display:none; width:100%; margin-top:12px;"><i class="fas fa-sync-alt"></i> Retry Connection</button>
      <button class="secondary" id="forgotPasswordBtn" style="width:100%; margin-top:18px;">Forgot password?</button>
    </div>

    <!-- Dashboard -->
    <div id="dashboardPanel" class="dashboard">
      <div class="dashboard-header">
        <h1>SchemeVault Admin</h1>
        <div class="header-actions">
          <button class="secondary" id="changePasswordBtn"><i class="fas fa-key"></i> Change</button>
          <button class="secondary" id="healthCheckBtn"><i class="fas fa-heartbeat"></i> Health</button>
          <button class="logout-btn" id="logoutBtn"><i class="fas fa-sign-out-alt"></i> Sign Out</button>
        </div>
      </div>
      
      <!-- Stats Overview -->
      <div class="card-grid">
        <div class="card">
          <h3><i class="fas fa-chart-pie" style="color:#059669;"></i> Overview</h3>
          <div class="stats-grid">
            <div class="stat-item"><div class="stat-value" id="statVisits">0</div><div class="stat-label">Visits</div></div>
            <div class="stat-item"><div class="stat-value" id="statDownloads">0</div><div class="stat-label">Downloads</div></div>
            <div class="stat-item"><div class="stat-value" id="statPayments">0</div><div class="stat-label">Sales (KES)</div></div>
            <div class="stat-item"><div class="stat-value" id="statActive">0</div><div class="stat-label">Active Users</div></div>
          </div>
        </div>
        <div class="card">
          <h3><i class="fas fa-book-open"></i> Learning Areas</h3>
          <div class="form-group"><label>New Subject</label><input type="text" id="newSubjectName" placeholder="e.g., Mathematics"></div>
          <button id="addSubjectBtn"><i class="fas fa-plus"></i> Add Subject</button>
          <div id="subjectList" style="margin-top:20px; max-height:220px; overflow-y:auto;"></div>
        </div>
      </div>

      <!-- Visitor Logs -->
      <div class="card">
        <h3><i class="fas fa-users"></i> Recent Visitors</h3>
        <div id="visitorLogs" class="visitor-log">Loading...</div>
        <button id="clearVisitorsBtn" class="danger small" style="margin-top:16px;"><i class="fas fa-trash-alt"></i> Clear All Logs</button>
      </div>

      <!-- Tabs -->
      <div class="tabs">
        <button class="tab active" data-tab="upload"><i class="fas fa-cloud-upload-alt"></i> Upload</button>
        <button class="tab" data-tab="schemes"><i class="fas fa-list"></i> Schemes</button>
        <button class="tab" data-tab="bulk"><i class="fas fa-layer-group"></i> Bulk Ops</button>
        <button class="tab" data-tab="analytics"><i class="fas fa-chart-bar"></i> Analytics</button>
        <button class="tab" data-tab="settings"><i class="fas fa-cog"></i> Settings</button>
        <button class="tab" data-tab="backup"><i class="fas fa-database"></i> Backup</button>
      </div>

      <!-- Upload Tab -->
      <div id="tab-upload" class="tab-content active">
        <div style="display:flex; gap:12px; margin-bottom:24px; flex-wrap:wrap;">
          <button id="showSingleUploadBtn" style="background:#059669; color:white;"><i class="fas fa-file"></i> Single Upload</button>
          <button id="showBulkUploadBtn" class="secondary"><i class="fas fa-files"></i> Bulk Upload</button>
        </div>
        
        <!-- Single Upload Form -->
        <form id="uploadForm" enctype="multipart/form-data" class="card">
          <div class="form-row">
            <div class="form-group"><label>Title *</label><input name="title" id="schemeTitle" required></div>
            <div class="form-group"><label>Grade *</label><input name="grade" id="schemeGrade" required></div>
          </div>
          <div class="form-row">
            <div class="form-group"><label>Subject *</label><select name="subject" id="schemeSubject" required></select></div>
            <div class="form-group"><label>Term *</label><select name="term" id="schemeTerm"><option value="1">Term 1</option><option value="2">Term 2</option><option value="3">Term 3</option></select></div>
          </div>
          <div class="form-row">
            <div class="form-group"><label>Weeks</label><input type="number" name="weeks" id="schemeWeeks"></div>
            <div class="form-group"><label>Price (KES) *</label><input type="number" name="price" id="schemePrice" required></div>
          </div>
          <div class="form-group"><label>Pages</label><input type="number" name="pages" id="schemePages"></div>
          <div class="form-row">
            <div class="form-group"><label>Document *</label><input type="file" name="document" accept=".pdf,.doc,.docx" required></div>
            <div class="form-group"><label>Cover Image</label><input type="file" name="cover" accept="image/*"></div>
          </div>
          <div class="form-row">
            <div class="form-group"><label>Publish At</label><input type="datetime-local" name="publishAt" id="schemePublishAt"></div>
            <div class="form-group"><label>Unpublish At</label><input type="datetime-local" name="unpublishAt" id="schemeUnpublishAt"></div>
          </div>
          <div class="form-group"><label><input type="checkbox" name="visible" id="schemeVisibility" checked> Visible on site</label></div>
          <div class="progress-container" id="singleProgressContainer" style="display:none;">
            <div class="progress-bar-wrapper">
              <progress id="uploadProgress" value="0" max="100"></progress>
              <span class="progress-percent" id="uploadPercent">0%</span>
            </div>
          </div>
          <button type="submit" id="uploadSubmitBtn"><i class="fas fa-check"></i> Upload Scheme</button>
          <p id="uploadStatus" style="margin-top:12px;"></p>
        </form>

        <!-- Bulk Upload Form -->
        <form id="bulkUploadForm" enctype="multipart/form-data" class="card" style="display:none;">
          <div class="form-row">
            <div class="form-group"><label>Base Title *</label><input name="title" id="bulkTitle" required></div>
            <div class="form-group"><label>Grade *</label><input name="grade" id="bulkGrade" required></div>
          </div>
          <div class="form-row">
            <div class="form-group"><label>Subject *</label><select name="subject" id="bulkSubject" required></select></div>
            <div class="form-group"><label>Term *</label><select name="term" id="bulkTerm"><option value="1">Term 1</option><option value="2">Term 2</option><option value="3">Term 3</option></select></div>
          </div>
          <div class="form-row">
            <div class="form-group"><label>Weeks</label><input type="number" name="weeks" id="bulkWeeks"></div>
            <div class="form-group"><label>Price *</label><input type="number" name="price" id="bulkPrice" required></div>
          </div>
          <div class="form-group"><label>Pages</label><input type="number" name="pages" id="bulkPages"></div>
          <div class="bulk-upload-area" id="dropZone">
            <i class="fas fa-cloud-upload-alt" style="font-size:2.5rem; color:#64748b; margin-bottom:8px;"></i>
            <p style="font-weight:500;">Drag & drop or click to select documents</p>
            <p style="font-size:0.85rem; color:#64748b;">Multiple PDF/DOC files</p>
            <input type="file" id="bulkDocuments" name="documents" multiple accept=".pdf,.doc,.docx" style="display:none;">
            <input type="file" id="bulkCovers" name="covers" multiple accept="image/*" style="display:none;">
          </div>
          <div style="display:flex; gap:12px; margin:20px 0; flex-wrap:wrap;">
            <button type="button" id="selectDocsBtn" class="secondary"><i class="fas fa-file-pdf"></i> Select Documents</button>
            <button type="button" id="selectCoversBtn" class="secondary"><i class="fas fa-image"></i> Select Covers</button>
          </div>
          <div id="selectedFilesList" style="margin-bottom:16px;"></div>
          <div class="form-group"><label><input type="checkbox" name="visible" id="bulkVisible" checked> Visible</label></div>
          <div class="progress-container" id="bulkProgressContainer" style="display:none;">
            <div class="progress-bar-wrapper">
              <progress id="bulkUploadProgress" value="0" max="100"></progress>
              <span class="progress-percent" id="bulkUploadPercent">0%</span>
            </div>
          </div>
          <button type="submit" id="bulkUploadSubmitBtn"><i class="fas fa-upload"></i> Upload All Schemes</button>
          <p id="bulkUploadStatus" style="margin-top:12px;"></p>
        </form>
      </div>

      <!-- Schemes Tab -->
      <div id="tab-schemes" class="tab-content">
        <div class="card">
          <h3><i class="fas fa-list-ul"></i> All Schemes</h3>
          <div id="allSchemesList" class="schemes-list"></div>
        </div>
      </div>

      <!-- Bulk Operations Tab -->
      <div id="tab-bulk" class="tab-content">
        <div class="card-grid">
          <div class="card">
            <h3><i class="fas fa-tags"></i> Bulk Price Update</h3>
            <div class="form-group"><label>Select Schemes</label><select id="bulkSchemeSelect" multiple style="height:150px;"></select></div>
            <div class="form-row">
              <div class="form-group"><label>Operation</label><select id="bulkPriceOp"><option value="set">Set to</option><option value="increase">Increase by</option><option value="decrease">Decrease by</option></select></div>
              <div class="form-group"><label>Amount (KES)</label><input type="number" id="bulkPriceAmount" min="0"></div>
            </div>
            <button id="applyBulkPriceBtn"><i class="fas fa-check"></i> Apply</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-eye-slash"></i> Bulk Visibility</h3>
            <div class="form-group"><label>Select Schemes</label><select id="bulkVisibilitySelect" multiple style="height:150px;"></select></div>
            <div class="form-group"><label>Set Visibility</label><select id="bulkVisibilityValue"><option value="true">Visible</option><option value="false">Hidden</option></select></div>
            <button id="applyBulkVisibilityBtn"><i class="fas fa-check"></i> Apply</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-star"></i> Featured Schemes</h3>
            <div class="form-group"><label>Select Featured</label><select id="featuredSchemeSelect" multiple style="height:150px;"></select></div>
            <button id="saveFeaturedBtn"><i class="fas fa-save"></i> Save Featured</button>
          </div>
        </div>
      </div>

      <!-- Analytics Tab -->
      <div id="tab-analytics" class="tab-content">
        <div class="card-grid">
          <div class="card">
            <h3><i class="fas fa-chart-line"></i> Top Selling Schemes</h3>
            <div id="analyticsList" style="max-height:400px; overflow-y:auto;"></div>
          </div>
          <div class="card">
            <h3><i class="fas fa-download"></i> Export Data</h3>
            <button id="exportSalesBtn"><i class="fas fa-file-csv"></i> Download Sales CSV</button>
            <button id="exportBackupBtn" class="secondary" style="margin-top:14px;"><i class="fas fa-archive"></i> Download Full Backup</button>
          </div>
        </div>
      </div>

      <!-- Settings Tab -->
      <div id="tab-settings" class="tab-content">
        <div class="card-grid">
          <div class="card">
            <h3><i class="fas fa-filter"></i> Grade Display</h3>
            <div class="form-group"><label><input type="radio" name="gradeDisplay" value="all" id="showAllGrades" checked> Show all grades</label></div>
            <div class="form-group"><label><input type="radio" name="gradeDisplay" value="content" id="showGradesWithContent"> Only grades with content</label></div>
            <button id="saveGradeDisplayBtn">Save Setting</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-envelope"></i> Email Notifications</h3>
            <div class="form-group"><label><input type="checkbox" id="emailNotificationsEnabled"> Send email on new sale</label></div>
            <button id="saveEmailNotificationsBtn">Save</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-bullhorn"></i> Scrolling Banner</h3>
            <div class="form-group"><label>Banner Text</label><input id="bannerText" placeholder="Promotional message"></div>
            <div class="form-group"><label><input type="checkbox" id="bannerEnabled"> Enable</label></div>
            <button id="saveBannerBtn">Save</button>
          </div>
          <div class="card">
            <h3><i class="fab fa-whatsapp"></i> WhatsApp Button</h3>
            <div class="form-group"><label>Number (254...)</label><input id="waNumber" placeholder="254712345678"></div>
            <div class="form-group"><label>Message</label><input id="waMessage" value="Hello"></div>
            <div class="form-group"><label><input type="checkbox" id="waEnabled"> Enable</label></div>
            <button id="saveWhatsAppBtn">Save</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-calendar-alt"></i> Term Visibility</h3>
            <div><label><input type="checkbox" id="term1Enabled" checked> Term 1</label></div>
            <div><label><input type="checkbox" id="term2Enabled" checked> Term 2</label></div>
            <div><label><input type="checkbox" id="term3Enabled" checked> Term 3</label></div>
            <div class="form-group"><label>Default Term</label><select id="defaultTerm"><option value="1">Term 1</option><option value="2">Term 2</option><option value="3">Term 3</option></select></div>
            <button id="saveTermsBtn">Save</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-graduation-cap"></i> Grades Management</h3>
            <div id="gradesList" style="max-height:200px; overflow-y:auto; margin-bottom:16px;"></div>
            <div class="form-group"><input id="newGradeName" placeholder="e.g., Grade 6"></div>
            <button id="addGradeBtn">Add Grade</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-comment-dots"></i> Engagement Popup</h3>
            <div class="form-group"><input id="popupQuestion" placeholder="Question"></div>
            <div class="form-group"><input id="popupOptions" placeholder="Options (comma separated)"></div>
            <div class="form-row">
              <div class="form-group">
                <label>Trigger</label>
                <select id="popupTrigger">
                  <option value="onload">On Page Load</option>
                  <option value="instant">Instant</option>
                  <option value="afterdownload">After Download</option>
                </select>
              </div>
              <div class="form-group">
                <label>Delay</label>
                <input type="number" id="popupDelay" min="0" value="0" placeholder="0">
              </div>
              <div class="form-group">
                <label>Unit</label>
                <select id="popupDelayUnit">
                  <option value="seconds">Seconds</option>
                  <option value="minutes">Minutes</option>
                </select>
              </div>
            </div>
            <div><label><input type="checkbox" id="popupWhatsapp"> Collect WhatsApp</label></div>
            <button id="savePopupBtn" style="margin-top:14px;">Save Popup</button>
          </div>
        </div>
      </div>

      <!-- Backup Tab -->
      <div id="tab-backup" class="tab-content">
        <div class="card-grid">
          <div class="card">
            <h3><i class="fas fa-download"></i> Backup Data</h3>
            <p style="margin-bottom:18px; color:#475569;">Download all data as a ZIP archive.</p>
            <button id="downloadBackupBtn"><i class="fas fa-archive"></i> Download Backup</button>
          </div>
          <div class="card">
            <h3><i class="fas fa-upload"></i> Restore Data</h3>
            <div class="form-group"><label>Select Backup File</label><input type="file" id="restoreFile" accept=".zip"></div>
            <button id="restoreBackupBtn"><i class="fas fa-undo-alt"></i> Restore from Backup</button>
            <p id="restoreStatus" style="margin-top:12px;"></p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Modals -->
  <div id="editModal" class="modal">
    <div class="modal-content">
      <h3>Edit Scheme</h3>
      <input type="hidden" id="editSchemeId">
      <div class="form-group"><label>Price (KES)</label><input type="number" id="editPrice"></div>
      <div class="form-group"><label>Weeks</label><input type="number" id="editWeeks"></div>
      <div class="form-row">
        <div class="form-group"><label>Publish At</label><input type="datetime-local" id="editPublishAt"></div>
        <div class="form-group"><label>Unpublish At</label><input type="datetime-local" id="editUnpublishAt"></div>
      </div>
      <div class="form-group"><label><input type="checkbox" id="editVisible"> Visible</label></div>
      <div class="form-group"><label>Replace Cover</label><input type="file" id="editCoverFile" accept="image/*"></div>
      <div style="display:flex; gap:12px; margin-top:24px;">
        <button id="saveEditBtn">Save Changes</button>
        <button class="secondary" id="cancelEditBtn">Cancel</button>
      </div>
    </div>
  </div>

  <div id="passwordModal" class="modal">
    <div class="modal-content">
      <h3>Change Password</h3>
      <div class="form-group"><label>New Password</label><input type="password" id="newPassword" placeholder="Minimum 6 characters"></div>
      <div class="form-group"><label>Confirm Password</label><input type="password" id="confirmPassword"></div>
      <div style="display:flex; gap:12px;">
        <button id="savePasswordBtn">Update</button>
        <button class="secondary" id="cancelPasswordBtn">Cancel</button>
      </div>
      <p id="passwordError" style="color:#dc2626; margin-top:14px;"></p>
    </div>
  </div>

  <div id="forgotModal" class="modal">
    <div class="modal-content">
      <h3>Reset Password</h3>
      <div id="step1">
        <p style="margin-bottom:16px;">A reset code will be sent to the admin email.</p>
        <button id="sendResetCodeBtn">Send Code</button>
        <p id="resetError" style="color:#dc2626;"></p>
      </div>
      <div id="step2" style="display:none;">
        <div class="form-group"><input id="resetCode" placeholder="6-digit code"></div>
        <div class="form-group"><input type="password" id="resetNewPassword" placeholder="New password"></div>
        <button id="resetPasswordBtn">Reset Password</button>
        <p id="resetStep2Error" style="color:#dc2626;"></p>
      </div>
      <button class="secondary" id="closeForgotModalBtn" style="margin-top:20px;">Cancel</button>
    </div>
  </div>

  <div id="healthModal" class="modal">
    <div class="modal-content">
      <h3>System Health</h3>
      <div id="healthContent">Loading...</div>
      <button class="secondary" id="closeHealthModalBtn" style="margin-top:20px;">Close</button>
    </div>
  </div>

  <script>
    (function() {
      const API_BASE = 'https://schemevault-backend.onrender.com';
      let token = localStorage.getItem('adminToken') || '';
      let subjects = [];
      let allSchemes = [];

      function showToast(msg, isError = false) {
        const toast = document.createElement('div');
        toast.className = 'toast' + (isError ? ' error' : '');
        toast.textContent = msg;
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 3000);
      }

      const retryBtn = document.getElementById('retryConnectionBtn');
      
      async function checkBackend() {
        const statusEl = document.getElementById('connectionStatus');
        statusEl.textContent = 'Checking...';
        statusEl.className = 'status-badge status-offline';
        retryBtn.style.display = 'none';
        
        const controller = new AbortController();
        const timeoutId = setTimeout(() => controller.abort(), 8000);
        
        try {
          const res = await fetch(`${API_BASE}/health`, { signal: controller.signal });
          clearTimeout(timeoutId);
          if (res.ok) {
            statusEl.textContent = 'Online';
            statusEl.className = 'status-badge status-online';
          } else {
            statusEl.textContent = 'Offline';
            retryBtn.style.display = 'block';
          }
        } catch (err) {
          clearTimeout(timeoutId);
          statusEl.textContent = 'Offline';
          retryBtn.style.display = 'block';
          console.warn('Health check:', err.message);
        }
      }
      
      retryBtn.addEventListener('click', checkBackend);

      async function login() {
        const pwd = document.getElementById('adminPassword').value.trim();
        if (!pwd) { document.getElementById('loginError').textContent = 'Enter password'; return; }
        try {
          const res = await fetch(`${API_BASE}/api/admin/login`, {
            method: 'POST',
            headers: {'Content-Type':'application/json'},
            body: JSON.stringify({password:pwd})
          });
          const data = await res.json();
          if (res.ok) {
            token = data.token;
            localStorage.setItem('adminToken', token);
            showDashboard();
            loadDashboardData();
          } else {
            document.getElementById('loginError').textContent = data.error || 'Invalid password';
          }
        } catch { document.getElementById('loginError').textContent = 'Network error'; }
      }

      function showDashboard() {
        document.getElementById('loginPanel').style.display = 'none';
        document.getElementById('dashboardPanel').style.display = 'block';
      }

      function logout() {
        localStorage.removeItem('adminToken');
        token = '';
        document.getElementById('loginPanel').style.display = 'block';
        document.getElementById('dashboardPanel').style.display = 'none';
      }

      async function loadDashboardData() {
        try {
          const statsRes = await fetch(`${API_BASE}/api/admin/stats`, { headers: {'X-Admin-Token':token} });
          const stats = await statsRes.json();
          document.getElementById('statVisits').textContent = stats.visits || 0;
          document.getElementById('statDownloads').textContent = stats.downloads || 0;
          document.getElementById('statPayments').textContent = (stats.sales || 0).toLocaleString();
          document.getElementById('statActive').textContent = stats.activeUsers || 0;

          const visitorsRes = await fetch(`${API_BASE}/api/admin/visitors`, { headers: {'X-Admin-Token':token} });
          const visitors = await visitorsRes.json();
          const visitorContainer = document.getElementById('visitorLogs');
          visitorContainer.innerHTML = visitors.slice(-20).reverse().map(v => 
            `<div>${new Date(v.time).toLocaleString()} - ${v.ip} (${v.device}, ${v.browser})</div>`
          ).join('') || 'No visitors yet.';

          await loadSubjects();

          const schemesRes = await fetch(`${API_BASE}/api/admin/schemes`, { headers: {'X-Admin-Token':token} });
          allSchemes = await schemesRes.json();
          renderSchemesList(allSchemes);
          populateBulkSelects(allSchemes);
          populateFeaturedSelect(allSchemes);

          const settingsRes = await fetch(`${API_BASE}/api/settings`);
          const settings = await settingsRes.json();
          document.getElementById('showAllGrades').checked = settings.showAllGrades !== false;
          document.getElementById('showGradesWithContent').checked = settings.showAllGrades === false;

          try {
            const emailRes = await fetch(`${API_BASE}/api/admin/settings/email-notifications`, { headers: {'X-Admin-Token':token} });
            const emailData = await emailRes.json();
            document.getElementById('emailNotificationsEnabled').checked = emailData.emailNotifications !== false;
          } catch(e) {}

          const bannerRes = await fetch(`${API_BASE}/api/admin/banner`, { headers: {'X-Admin-Token':token} });
          const banner = await bannerRes.json();
          document.getElementById('bannerText').value = banner.text || '';
          document.getElementById('bannerEnabled').checked = banner.enabled || false;

          const waRes = await fetch(`${API_BASE}/api/admin/whatsapp`, { headers: {'X-Admin-Token':token} });
          const wa = await waRes.json();
          document.getElementById('waNumber').value = wa.number || '';
          document.getElementById('waMessage').value = wa.message || 'Hello';
          document.getElementById('waEnabled').checked = wa.enabled || false;

          const termsRes = await fetch(`${API_BASE}/api/admin/terms`, { headers: {'X-Admin-Token':token} });
          const terms = await termsRes.json();
          document.getElementById('term1Enabled').checked = terms.term1Enabled !== false;
          document.getElementById('term2Enabled').checked = terms.term2Enabled !== false;
          document.getElementById('term3Enabled').checked = terms.term3Enabled !== false;
          document.getElementById('defaultTerm').value = terms.defaultTerm || '1';

          const gradesRes = await fetch(`${API_BASE}/api/admin/grades`, { headers: {'X-Admin-Token':token} });
          const grades = await gradesRes.json();
          renderGradesList(grades);

          const popupRes = await fetch(`${API_BASE}/api/admin/popups`, { headers: {'X-Admin-Token':token} });
          const popups = await popupRes.json();
          if (popups.length) {
            const p = popups[0];
            document.getElementById('popupQuestion').value = p.question || '';
            document.getElementById('popupOptions').value = (p.options || []).join(', ');
            document.getElementById('popupTrigger').value = p.trigger || 'onload';
            document.getElementById('popupWhatsapp').checked = p.collectWhatsapp || false;
            document.getElementById('popupDelay').value = p.delay || 0;
            document.getElementById('popupDelayUnit').value = p.delayUnit || 'seconds';
          }

          loadAnalytics();
        } catch (e) { console.error(e); }
      }

      async function loadSubjects() {
        try {
          const res = await fetch(`${API_BASE}/api/admin/subjects`, { headers: {'X-Admin-Token':token} });
          if (!res.ok) { subjects = []; } else { subjects = await res.json(); }
        } catch { subjects = []; }
        renderSubjectList();
        renderSubjectSelects();
      }

      function renderSubjectList() {
        const container = document.getElementById('subjectList');
        if (!subjects.length) { container.innerHTML = '<p style="color:#64748b; text-align:center;">No subjects yet.</p>'; return; }
        container.innerHTML = subjects.map(s => `<div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px solid #edf2f7;"><span>${escapeHtml(s.name)}</span><button class="danger small" onclick="deleteSubject('${s.id}')"><i class="fas fa-trash"></i></button></div>`).join('');
      }

      function renderSubjectSelects() {
        const options = subjects.map(s => `<option value="${escapeHtml(s.name)}">${escapeHtml(s.name)}</option>`).join('');
        document.getElementById('schemeSubject').innerHTML = options;
        document.getElementById('bulkSubject').innerHTML = options;
      }

      function renderSchemesList(schemes) {
        const container = document.getElementById('allSchemesList');
        if (!schemes.length) { container.innerHTML = '<p style="color:#64748b; text-align:center;">No schemes yet.</p>'; return; }
        container.innerHTML = schemes.map(s => `
          <div class="scheme-item">
            <div class="scheme-info">
              <h4>${escapeHtml(s.title)}</h4>
              <small>${escapeHtml(s.grade)} | ${escapeHtml(s.subject)} | Term ${s.term} | KES ${s.price} | ${s.visible ? '✅' : '👁️'}</small>
              ${s.publishAt ? `<small>📅 Publishes: ${new Date(s.publishAt).toLocaleString()}</small>` : ''}
            </div>
            <div class="scheme-actions">
              <button onclick="editScheme('${s.id}')" class="small"><i class="fas fa-edit"></i> Edit</button>
              <button class="danger small" onclick="deleteScheme('${s.id}')"><i class="fas fa-trash"></i> Delete</button>
            </div>
          </div>
        `).join('');
      }

      function populateBulkSelects(schemes) {
        const options = schemes.map(s => `<option value="${s.id}">${escapeHtml(s.title)} (${s.grade}) - KES ${s.price}</option>`).join('');
        document.getElementById('bulkSchemeSelect').innerHTML = options;
        document.getElementById('bulkVisibilitySelect').innerHTML = options;
      }

      function populateFeaturedSelect(schemes) {
        const select = document.getElementById('featuredSchemeSelect');
        fetch(`${API_BASE}/api/admin/schemes/featured`, { headers: {'X-Admin-Token':token} })
          .then(r => r.json())
          .then(data => {
            const featuredIds = data.featuredSchemeIds || [];
            select.innerHTML = schemes.map(s => `<option value="${s.id}" ${featuredIds.includes(s.id) ? 'selected' : ''}>${escapeHtml(s.title)} (${s.grade})</option>`).join('');
          });
      }

      function renderGradesList(grades) {
        const container = document.getElementById('gradesList');
        if (!grades.length) { container.innerHTML = '<p style="color:#64748b;">No grades.</p>'; return; }
        container.innerHTML = grades.map(g => `<div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px solid #edf2f7;"><span>${escapeHtml(g.name)}</span><button class="danger small" onclick="deleteGrade('${g.id}')"><i class="fas fa-trash"></i></button></div>`).join('');
      }

      async function loadAnalytics() {
        try {
          const res = await fetch(`${API_BASE}/api/admin/analytics/downloads`, { headers: {'X-Admin-Token':token} });
          const data = await res.json();
          document.getElementById('analyticsList').innerHTML = data.slice(0,20).map(s => `<div style="display:flex; justify-content:space-between; padding:8px 0;"><span>${escapeHtml(s.title)}</span><span>${s.downloads} (KES ${s.revenue})</span></div>`).join('');
        } catch(e) {}
      }

      window.deleteSubject = async (id) => { if(confirm('Delete?')) { await fetch(`${API_BASE}/api/admin/subjects/${id}`, { method:'DELETE', headers:{'X-Admin-Token':token} }); loadDashboardData(); } };
      window.deleteScheme = async (id) => { if(confirm('Delete?')) { await fetch(`${API_BASE}/api/admin/schemes/${id}`, { method:'DELETE', headers:{'X-Admin-Token':token} }); loadDashboardData(); } };
      window.deleteGrade = async (id) => { if(confirm('Delete?')) { await fetch(`${API_BASE}/api/admin/grades/${id}`, { method:'DELETE', headers:{'X-Admin-Token':token} }); loadDashboardData(); } };
      window.editScheme = (id) => {
        const scheme = allSchemes.find(s => s.id === id);
        if (!scheme) return;
        document.getElementById('editSchemeId').value = id;
        document.getElementById('editPrice').value = scheme.price;
        document.getElementById('editWeeks').value = scheme.weeks || '';
        document.getElementById('editVisible').checked = scheme.visible !== false;
        document.getElementById('editPublishAt').value = scheme.publishAt?.slice(0,16) || '';
        document.getElementById('editUnpublishAt').value = scheme.unpublishAt?.slice(0,16) || '';
        document.getElementById('editCoverFile').value = '';
        document.getElementById('editModal').classList.add('open');
      };

      // Event Listeners
      document.getElementById('loginBtn').addEventListener('click', login);
      document.getElementById('logoutBtn').addEventListener('click', logout);
      document.getElementById('adminPassword').addEventListener('keypress', e => { if(e.key==='Enter') login(); });
      document.querySelectorAll('.tab').forEach(t => t.addEventListener('click', function() {
        document.querySelectorAll('.tab').forEach(x => x.classList.remove('active'));
        document.querySelectorAll('.tab-content').forEach(x => x.classList.remove('active'));
        this.classList.add('active');
        document.getElementById(`tab-${this.dataset.tab}`).classList.add('active');
      }));

      document.getElementById('showSingleUploadBtn').addEventListener('click', () => { document.getElementById('uploadForm').style.display='block'; document.getElementById('bulkUploadForm').style.display='none'; });
      document.getElementById('showBulkUploadBtn').addEventListener('click', () => { document.getElementById('uploadForm').style.display='none'; document.getElementById('bulkUploadForm').style.display='block'; });
      document.getElementById('selectDocsBtn').addEventListener('click', () => document.getElementById('bulkDocuments').click());
      document.getElementById('selectCoversBtn').addEventListener('click', () => document.getElementById('bulkCovers').click());
      document.getElementById('dropZone').addEventListener('click', () => document.getElementById('bulkDocuments').click());
      document.getElementById('bulkDocuments').addEventListener('change', () => { document.getElementById('selectedFilesList').innerHTML = `<p>${document.getElementById('bulkDocuments').files.length} document(s) selected.</p>`; });

      document.getElementById('addSubjectBtn').addEventListener('click', async () => {
        const name = document.getElementById('newSubjectName').value.trim();
        if (!name) return showToast('Enter name', true);
        const res = await fetch(`${API_BASE}/api/admin/subjects`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({name}) });
        if (res.ok) { document.getElementById('newSubjectName').value = ''; loadDashboardData(); showToast('Subject added'); }
        else { const d = await res.json(); showToast(d.error || 'Failed', true); }
      });

      document.getElementById('clearVisitorsBtn').addEventListener('click', async () => { if(confirm('Clear?')) { await fetch(`${API_BASE}/api/admin/visitors/clear`, { method:'DELETE', headers:{'X-Admin-Token':token} }); loadDashboardData(); } });

      document.getElementById('saveGradeDisplayBtn').addEventListener('click', async () => {
        await fetch(`${API_BASE}/api/admin/settings/grade-display`, { method:'PATCH', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({showAllGrades: document.getElementById('showAllGrades').checked}) });
        showToast('Saved');
      });
      document.getElementById('saveEmailNotificationsBtn').addEventListener('click', async () => {
        await fetch(`${API_BASE}/api/admin/settings/email-notifications`, { method:'PATCH', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({enabled: document.getElementById('emailNotificationsEnabled').checked}) });
        showToast('Saved');
      });
      document.getElementById('saveBannerBtn').addEventListener('click', async () => {
        await fetch(`${API_BASE}/api/admin/banner`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({text: document.getElementById('bannerText').value, enabled: document.getElementById('bannerEnabled').checked}) });
        showToast('Saved');
      });
      document.getElementById('saveWhatsAppBtn').addEventListener('click', async () => {
        await fetch(`${API_BASE}/api/admin/whatsapp`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({number: document.getElementById('waNumber').value, message: document.getElementById('waMessage').value, enabled: document.getElementById('waEnabled').checked}) });
        showToast('Saved');
      });
      document.getElementById('saveTermsBtn').addEventListener('click', async () => {
        await fetch(`${API_BASE}/api/admin/terms`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({
          term1Enabled: document.getElementById('term1Enabled').checked, term2Enabled: document.getElementById('term2Enabled').checked, term3Enabled: document.getElementById('term3Enabled').checked, defaultTerm: document.getElementById('defaultTerm').value
        })});
        showToast('Saved');
      });
      document.getElementById('addGradeBtn').addEventListener('click', async () => {
        const name = document.getElementById('newGradeName').value.trim();
        if (!name) return showToast('Enter name', true);
        await fetch(`${API_BASE}/api/admin/grades`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({name}) });
        document.getElementById('newGradeName').value = ''; loadDashboardData();
      });
      document.getElementById('savePopupBtn').addEventListener('click', async () => {
        const question = document.getElementById('popupQuestion').value.trim();
        const options = document.getElementById('popupOptions').value.split(',').map(s=>s.trim()).filter(s=>s);
        const trigger = document.getElementById('popupTrigger').value;
        const collectWhatsapp = document.getElementById('popupWhatsapp').checked;
        const delay = document.getElementById('popupDelay').value;
        const delayUnit = document.getElementById('popupDelayUnit').value;
        if (!question) return showToast('Enter question', true);
        await fetch(`${API_BASE}/api/admin/popups`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({question, options, trigger, collectWhatsapp, delay, delayUnit}) });
        showToast('Saved');
      });

      document.getElementById('applyBulkPriceBtn').addEventListener('click', async () => {
        const ids = Array.from(document.getElementById('bulkSchemeSelect').selectedOptions).map(o=>o.value);
        const amount = document.getElementById('bulkPriceAmount').value;
        const op = document.getElementById('bulkPriceOp').value;
        if (!ids.length || !amount) return showToast('Select schemes and amount', true);
        const res = await fetch(`${API_BASE}/api/admin/schemes/bulk-price`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({schemeIds:ids, price:Number(amount), operation:op}) });
        const d = await res.json(); showToast(`Updated ${d.updated}`); loadDashboardData();
      });
      document.getElementById('applyBulkVisibilityBtn').addEventListener('click', async () => {
        const ids = Array.from(document.getElementById('bulkVisibilitySelect').selectedOptions).map(o=>o.value);
        const visible = document.getElementById('bulkVisibilityValue').value === 'true';
        if (!ids.length) return showToast('Select schemes', true);
        const res = await fetch(`${API_BASE}/api/admin/schemes/bulk-visibility`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({schemeIds:ids, visible}) });
        const d = await res.json(); showToast(`Updated ${d.updated}`); loadDashboardData();
      });
      document.getElementById('saveFeaturedBtn').addEventListener('click', async () => {
        const ids = Array.from(document.getElementById('featuredSchemeSelect').selectedOptions).map(o=>o.value);
        await fetch(`${API_BASE}/api/admin/schemes/featured`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({schemeIds:ids}) });
        showToast('Saved');
      });

      document.getElementById('exportSalesBtn').addEventListener('click', () => window.open(`${API_BASE}/api/admin/sales/export?token=${token}`));
      document.getElementById('exportBackupBtn').addEventListener('click', () => window.open(`${API_BASE}/api/admin/backup?token=${token}`));
      document.getElementById('downloadBackupBtn').addEventListener('click', () => window.open(`${API_BASE}/api/admin/backup?token=${token}`));
      document.getElementById('restoreBackupBtn').addEventListener('click', async () => {
        const file = document.getElementById('restoreFile').files[0];
        if (!file) return showToast('Select file', true);
        const fd = new FormData(); fd.append('backup', file);
        const res = await fetch(`${API_BASE}/api/admin/restore`, { method:'POST', headers:{'X-Admin-Token':token}, body:fd });
        if (res.ok) { showToast('Restored! Reloading...'); setTimeout(()=>location.reload(),2000); }
        else showToast('Failed', true);
      });

      document.getElementById('healthCheckBtn').addEventListener('click', async () => {
        const modal = document.getElementById('healthModal'), content = document.getElementById('healthContent');
        modal.classList.add('open'); content.innerHTML = 'Loading...';
        const res = await fetch(`${API_BASE}/api/admin/health`, { headers:{'X-Admin-Token':token} });
        const d = await res.json();
        content.innerHTML = `<p>B2: ${d.b2.status}</p><p>Schemes: ${d.database.schemes}</p><p>Subjects: ${d.database.subjects}</p>`;
      });
      document.getElementById('closeHealthModalBtn').addEventListener('click', () => document.getElementById('healthModal').classList.remove('open'));

      document.getElementById('saveEditBtn').addEventListener('click', async () => {
        const id = document.getElementById('editSchemeId').value;
        const price = document.getElementById('editPrice').value;
        const weeks = document.getElementById('editWeeks').value;
        const visible = document.getElementById('editVisible').checked;
        const publishAt = document.getElementById('editPublishAt').value;
        const unpublishAt = document.getElementById('editUnpublishAt').value;
        const coverFile = document.getElementById('editCoverFile').files[0];
        await fetch(`${API_BASE}/api/admin/schemes/${id}`, { method:'PATCH', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({price:Number(price), weeks:Number(weeks)||null, visible, publishAt: publishAt||null, unpublishAt: unpublishAt||null}) });
        if (coverFile) { const fd = new FormData(); fd.append('cover', coverFile); await fetch(`${API_BASE}/api/admin/schemes/${id}/cover`, { method:'POST', headers:{'X-Admin-Token':token}, body:fd }); }
        document.getElementById('editModal').classList.remove('open'); loadDashboardData(); showToast('Updated');
      });
      document.getElementById('cancelEditBtn').addEventListener('click', () => document.getElementById('editModal').classList.remove('open'));

      document.getElementById('changePasswordBtn').addEventListener('click', () => document.getElementById('passwordModal').classList.add('open'));
      document.getElementById('cancelPasswordBtn').addEventListener('click', () => document.getElementById('passwordModal').classList.remove('open'));
      document.getElementById('savePasswordBtn').addEventListener('click', async () => {
        const np = document.getElementById('newPassword').value, cp = document.getElementById('confirmPassword').value;
        if (np !== cp) return document.getElementById('passwordError').textContent = 'Mismatch';
        if (np.length < 6) return document.getElementById('passwordError').textContent = 'Too short';
        const res = await fetch(`${API_BASE}/api/admin/change-password`, { method:'POST', headers:{'Content-Type':'application/json','X-Admin-Token':token}, body:JSON.stringify({newPassword:np}) });
        if (res.ok) { document.getElementById('passwordModal').classList.remove('open'); showToast('Changed'); }
        else document.getElementById('passwordError').textContent = 'Failed';
      });

      document.getElementById('forgotPasswordBtn').addEventListener('click', () => document.getElementById('forgotModal').classList.add('open'));
      document.getElementById('closeForgotModalBtn').addEventListener('click', () => document.getElementById('forgotModal').classList.remove('open'));
      document.getElementById('sendResetCodeBtn').addEventListener('click', async () => {
        const res = await fetch(`${API_BASE}/api/admin/forgot-password`, { method:'POST' });
        const d = await res.json();
        if (res.ok) { document.getElementById('step1').style.display='none'; document.getElementById('step2').style.display='block'; if(d.demoCode) alert('Code: '+d.demoCode); }
        else document.getElementById('resetError').textContent = 'Failed';
      });
      document.getElementById('resetPasswordBtn').addEventListener('click', async () => {
        const code = document.getElementById('resetCode').value, np = document.getElementById('resetNewPassword').value;
        const res = await fetch(`${API_BASE}/api/admin/reset-password`, { method:'POST', headers:{'Content-Type':'application/json'}, body:JSON.stringify({code, newPassword:np}) });
        if (res.ok) { document.getElementById('forgotModal').classList.remove('open'); showToast('Reset'); }
        else document.getElementById('resetStep2Error').textContent = 'Invalid';
      });

      // Single Upload with Progress
      document.getElementById('uploadForm').addEventListener('submit', (e) => {
        e.preventDefault();
        const formData = new FormData(document.getElementById('uploadForm'));
        formData.set('visible', document.getElementById('schemeVisibility').checked);
        const progressContainer = document.getElementById('singleProgressContainer');
        const progressBar = document.getElementById('uploadProgress');
        const percentSpan = document.getElementById('uploadPercent');
        const submitBtn = document.getElementById('uploadSubmitBtn');
        progressContainer.style.display = 'block';
        progressBar.value = 0;
        percentSpan.textContent = '0%';
        submitBtn.disabled = true;
        const xhr = new XMLHttpRequest();
        xhr.open('POST', `${API_BASE}/api/admin/schemes`);
        xhr.setRequestHeader('X-Admin-Token', token);
        xhr.upload.onprogress = (e) => {
          if (e.lengthComputable) {
            const percent = Math.round((e.loaded / e.total) * 100);
            progressBar.value = percent;
            percentSpan.textContent = percent + '%';
          }
        };
        xhr.onload = () => {
          progressContainer.style.display = 'none';
          submitBtn.disabled = false;
          if (xhr.status === 201) { document.getElementById('uploadForm').reset(); loadDashboardData(); showToast('Uploaded'); }
          else showToast('Failed', true);
        };
        xhr.onerror = () => { progressContainer.style.display = 'none'; submitBtn.disabled = false; showToast('Network error', true); };
        xhr.send(formData);
      });

      // Bulk Upload with Progress
      document.getElementById('bulkUploadForm').addEventListener('submit', (e) => {
        e.preventDefault();
        const formData = new FormData(document.getElementById('bulkUploadForm'));
        formData.set('visible', document.getElementById('bulkVisible').checked);
        const progressContainer = document.getElementById('bulkProgressContainer');
        const progressBar = document.getElementById('bulkUploadProgress');
        const percentSpan = document.getElementById('bulkUploadPercent');
        const submitBtn = document.getElementById('bulkUploadSubmitBtn');
        progressContainer.style.display = 'block';
        progressBar.value = 0;
        percentSpan.textContent = '0%';
        submitBtn.disabled = true;
        const xhr = new XMLHttpRequest();
        xhr.open('POST', `${API_BASE}/api/admin/schemes/bulk`);
        xhr.setRequestHeader('X-Admin-Token', token);
        xhr.upload.onprogress = (e) => {
          if (e.lengthComputable) {
            const percent = Math.round((e.loaded / e.total) * 100);
            progressBar.value = percent;
            percentSpan.textContent = percent + '%';
          }
        };
        xhr.onload = () => {
          progressContainer.style.display = 'none';
          submitBtn.disabled = false;
          if (xhr.status === 201) { document.getElementById('bulkUploadForm').reset(); loadDashboardData(); showToast('Bulk upload complete'); }
          else showToast('Failed', true);
        };
        xhr.onerror = () => { progressContainer.style.display = 'none'; submitBtn.disabled = false; showToast('Network error', true); };
        xhr.send(formData);
      });

      function escapeHtml(s) { return String(s).replace(/[&<>"]/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c])); }

      checkBackend();
      if (token) { fetch(`${API_BASE}/api/admin/verify`, { headers:{'X-Admin-Token':token} }).then(r => r.ok ? (showDashboard(), loadDashboardData()) : logout()).catch(logout); }
    })();
  </script>
</body>
</html>