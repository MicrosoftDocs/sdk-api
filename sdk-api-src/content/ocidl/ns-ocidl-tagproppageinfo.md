---
UID: NS:ocidl.tagPROPPAGEINFO
title: tagPROPPAGEINFO
author: windows-sdk-content
description: Contains parameters used to describe a property page to a property frame. A property page fills a caller-provided structure in the IPropertyPage::GetPageInfo method.
old-location: com\proppageinfo.htm
tech.root: com
ms.assetid: 363fd45f-fb36-41f0-9d72-dc9c018859ec
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*LPPROPPAGEINFO, LPPROPPAGEINFO, LPPROPPAGEINFO structure pointer [COM], PROPPAGEINFO, PROPPAGEINFO structure [COM], _ctrl_PROPPAGEINFO, com.proppageinfo, ocidl/LPPROPPAGEINFO, ocidl/PROPPAGEINFO, tagPROPPAGEINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - PROPPAGEINFO
product: Windows
targetos: Windows
req.typenames: PROPPAGEINFO, *LPPROPPAGEINFO
req.redist: 
---

# tagPROPPAGEINFO structure


## -description


Contains parameters used to describe a property page to a property frame. A property page fills a caller-provided structure in the <a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">IPropertyPage::GetPageInfo</a> method.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field pszTitle

Pointer to an <a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a> that contains the string that appears in the tab for this page. The string must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. The caller of <a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field size

Required dimensions of the page's dialog box, in pixels.


### -field pszDocString

Pointer to a text string describing the page, which can be displayed in the property sheet dialog box (current frame implementation doesn't use this field). The text must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. The caller of <a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field pszHelpFile

Pointer to an <a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a> that contains the simple name of the help file that describes this property page used instead of implementing <a href="https://msdn.microsoft.com/ba715518-1aa0-42de-bad7-f2d0d0f00460">IPropertyPage::Help</a>. When the user presses Help, the Help method is normally called. If that method fails, the frame will open the help system with this help file (prefixed with the value of the HelpDir key in the property page's registry entries under its CLSID) and will instruct the help system to display the context described by the <b>dwHelpContext</b> field. The path must be allocated with <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. The caller of <a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">IPropertyPage::GetPageInfo</a> is responsible for freeing the memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field dwHelpContext

Context identifier for the help topic within <b>pszHelpFile</b> that describes this page.


## -remarks



The <b>pszTitle</b>, <b>pszDocString</b>, and the <b>pszHelpFile</b> members specified in this structure should contain text sensitive to the locale obtained through <a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cb7168c-bb05-4e01-a73b-11a52c5e690b">IPropertyPage::GetPageInfo</a>



<a href="https://msdn.microsoft.com/d569346d-4a40-42a4-ac8e-539588c4dd66">IPropertyPageSite::GetLocaleID</a>



<a href="https://msdn.microsoft.com/bf3341a0-5b1d-479b-998d-a61bb945e0c3">OLESTR</a>
 

 

