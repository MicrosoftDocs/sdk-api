---
UID: NS:commdlg._OFNOTIFYA
title: "_OFNOTIFYA"
author: windows-sdk-content
description: Contains information about a WM_NOTIFY message sent to an OFNHookProc hook procedure for an Open or Save As dialog box. The lParam parameter of the WM_NOTIFY message is a pointer to an OFNOTIFY structure.
old-location: dlgbox\ofnotify_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\ofnotify.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPOFNOTIFYA, LPOFNOTIFY, LPOFNOTIFY structure pointer [Dialog Boxes], OFNOTIFY, OFNOTIFY structure [Dialog Boxes], OFNOTIFYA, OFNOTIFYW, _OFNOTIFYA, _win32_OFNOTIFY_str, _win32_ofnotify_str_cpp, commdlg/LPOFNOTIFY, commdlg/OFNOTIFY, commdlg/OFNOTIFYA, commdlg/OFNOTIFYW, dlgbox.ofnotify_str, winui._win32_ofnotify_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commdlg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OFNOTIFYW (Unicode) and OFNOTIFYA (ANSI)
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
 - Commdlg.h
api_name:
 - OFNOTIFY
 - OFNOTIFYA
 - OFNOTIFYW
product: Windows
targetos: Windows
req.typenames: OFNOTIFYA, *LPOFNOTIFYA
req.redist: 
---

# _OFNOTIFYA structure


## -description


Contains information about a <a href="https://msdn.microsoft.com/en-us/library/Bb775583(v=VS.85).aspx">WM_NOTIFY</a> message sent to an <a href="https://msdn.microsoft.com/en-us/library/ms646931(v=VS.85).aspx">OFNHookProc</a> hook procedure for an <b>Open</b> or <b>Save As</b> dialog box. The <i>lParam</i> parameter of the <b>WM_NOTIFY</b> message is a pointer to an <b>OFNOTIFY</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

The <b>code</b> member of this structure can be one of the following notification messages that identify the message being sent: <a href="https://msdn.microsoft.com/en-us/library/ms646857(v=VS.85).aspx">CDN_FILEOK</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646859(v=VS.85).aspx">CDN_FOLDERCHANGE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646860(v=VS.85).aspx">CDN_HELP</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646863(v=VS.85).aspx">CDN_INITDONE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646865(v=VS.85).aspx">CDN_SELCHANGE</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646866(v=VS.85).aspx">CDN_SHAREVIOLATION</a>, <a href="https://msdn.microsoft.com/en-us/library/ms646868(v=VS.85).aspx">CDN_TYPECHANGE</a>. 


### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure that was specified when the <b>Open</b> or <b>Save As</b> dialog box was created. For some of the notification messages, this structure contains additional information about the event that caused the notification. 


### -field pszFile

Type: <b>LPTSTR</b>

The file name for which a network sharing violation has occurred. This member is valid only with the <a href="https://msdn.microsoft.com/en-us/library/ms646866(v=VS.85).aspx">CDN_SHAREVIOLATION</a> notification message. 


## -remarks



Not all of the <b>Open</b> and <b>Save As</b> notification messages use the <b>OFNOTIFY</b> structure. The <a href="https://msdn.microsoft.com/en-us/library/ms646862(v=VS.85).aspx">CDN_INCLUDEITEM</a> notification message uses the <a href="https://msdn.microsoft.com/en-us/library/ms646837(v=VS.85).aspx">OFNOTIFYEX</a> structure. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646857(v=VS.85).aspx">CDN_FILEOK</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646859(v=VS.85).aspx">CDN_FOLDERCHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646860(v=VS.85).aspx">CDN_HELP</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646863(v=VS.85).aspx">CDN_INITDONE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646865(v=VS.85).aspx">CDN_SELCHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646866(v=VS.85).aspx">CDN_SHAREVIOLATION</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646868(v=VS.85).aspx">CDN_TYPECHANGE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646837(v=VS.85).aspx">OFNOTIFYEX</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a>



<b>Reference</b>
 

 

