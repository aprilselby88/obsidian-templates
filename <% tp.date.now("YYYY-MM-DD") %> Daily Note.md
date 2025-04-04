##  🗓️ Meetings


## ✅ Do
<%*  
let prevNotePath = tp.date.now("YYYY-MM-DD", -1) + ".md";  
let prevNoteFile = app.vault.getAbstractFileByPath(prevNotePath);  
if (prevNoteFile) {  
    let prevContent = await app.vault.read(prevNoteFile);

	console.log(prevContent)
    
    // Normalize spaces in headings
    stripped = prevContent.replace(/##\s+/g, "## ");  

	console.log(stripped)

    let match = stripped.split("## ✅ Do")[1];  
    tR += match ? match.split("##")[0].trim() : "- [ ] No previous tasks found.";  
} else {  
    tR += "- [ ] No previous note found.";  
}  
%>

## 🔄 Chase
<%*  
if (prevNoteFile) {  
    let match = stripped.split("## 🔄 Chase")[1];  
    tR += match ? match.split("##")[0].trim() : "- [ ] No previous chase items found.";  
} else {  
    tR += "- [ ] No previous note found.";  
}  
%>

## 🔍 Review
<%*  
if (prevNoteFile) {  
    let match = stripped.split("## 🔍 Review")[1];  
    tR += match ? match.split("##")[0].trim() : "- [ ] No previous review items found.";  
} else {  
    tR += "- [ ] No previous note found.";  
}  
%>

## 🚀 Features to Work On
<%*  
if (prevNoteFile) {  
    let match = stripped.split("## 🚀 Features to Work On")[1];  
    tR += match ? match.split("##")[0].trim() : "- No previous features found.";  
} else {  
    tR += "- No previous note found.";  
}  
%>

## 🤝 1:1 Items Gathering

| Person | Discussion Points |
|--------|------------------|
<%*  
if (prevNoteFile) {  
    let match = stripped.split("| Person | Discussion Points |")[1];  
    tR += match ? match.trim() : "|        |                  |";  
} else {  
    tR += "|        |                  |";  
}  
%>