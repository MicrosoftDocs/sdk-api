---
UID: NS:ocidl.tagPROPPAGEINFO
title: PROPPAGEINFO (ocidl.h)
description: Contains parameters used to describe a property page to a property frame. A property page fills a caller-provided structure in the IPropertyPage::GetPageInfo method.
helpviewer_keywords: ["*LPPROPPAGEINFO","LPPROPPAGEINFO","LPPROPPAGEINFO structure pointer [COM]","PROPPAGEINFO","PROPPAGEINFO structure [COM]","_ctrl_PROPPAGEINFO","com.proppageinfo","ocidl/LPPROPPAGEINFO","ocidl/PROPPAGEINFO"]
old-location: com\proppageinfo.htm
tech.root: com
ms.assetid: 363fd45f-fb36-41f0-9d72-dc9c018859ec
ms.date: 12/05/2018
ms.keywords: '*LPPROPPAGEINFO, LPPROPPAGEINFO, LPPROPPAGEINFO structure pointer [COM], PROPPAGEINFO, PROPPAGEINFO structure [COM], _ctrl_PROPPAGEINFO, com.proppageinfo, ocidl/LPPROPPAGEINFO, ocidl/PROPPAGEINFO'
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROPPAGEINFO, *LPPROPPAGEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPROPPAGEINFO
 - ocidl/tagPROPPAGEINFO
 - LPPROPPAGEINFO
 - ocidl/LPPROPPAGEINFO
 - PROPPAGEINFO
 - ocidl/PROPPAGEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - PROPPAGEINFO
---

# PROPPAGEINFO structure


## -description

Contains parameters used to describe a property page to a property frame. A property page fills a caller-provided structure in the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a> method.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field pszTitle

Pointer to an <a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a> that contains the string that appears in the tab for this page. The string must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The caller of <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field size

Required dimensions of the page's dialog box, in pixels.

### -field pszDocString

Pointer to a text string describing the page, which can be displayed in the property sheet dialog box (current frame implementation doesn't use this field). The text must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The caller of <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field pszHelpFile

Pointer to an <a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a> that contains the simple name of the help file that describes this property page used instead of implementing <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-help">IPropertyPage::Help</a>. When the user presses Help, the Help method is normally called. If that method fails, the frame will open the help system with this help file (prefixed with the value of the HelpDir key in the property page's registry entries under its CLSID) and will instruct the help system to display the context described by the <b>dwHelpContext</b> field. The path must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The caller of <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field dwHelpContext

Context identifier for the help topic within <b>pszHelpFile</b> that describes this page.

## -remarks

The <b>pszTitle</b>, <b>pszDocString</b>, and the <b>pszHelpFile</b> members specified in this structure should contain text sensitive to the locale obtained through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>



<a href="/windows/desktop/api/wtypesbase/nf-wtypesbase-olestr">OLESTR</a>