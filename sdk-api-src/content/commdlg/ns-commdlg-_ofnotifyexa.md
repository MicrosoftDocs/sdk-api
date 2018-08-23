---
UID: NS:commdlg._OFNOTIFYEXA
title: "_OFNOTIFYEXA"
author: windows-sdk-content
description: Contains information about a CDN_INCLUDEITEM notification message.
old-location: dlgbox\ofnotifyex_str.htm
old-project: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\ofnotifyex.htm
ms.author: windowssdkdev
ms.date: 08/21/2018
ms.keywords: "*LPOFNOTIFYEXA, LPOFNOTIFYEX, LPOFNOTIFYEX structure pointer [Dialog Boxes], OFNOTIFYEX, OFNOTIFYEX structure [Dialog Boxes], OFNOTIFYEXA, OFNOTIFYEXW, _OFNOTIFYEXA, _win32_OFNOTIFYEX_str, _win32_ofnotifyex_str_cpp, commdlg/LPOFNOTIFYEX, commdlg/OFNOTIFYEX, commdlg/OFNOTIFYEXA, commdlg/OFNOTIFYEXW, dlgbox.ofnotifyex_str, winui._win32_ofnotifyex_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commdlg.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OFNOTIFYEXW (Unicode) and OFNOTIFYEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYEXA, *LPOFNOTIFYEXA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commdlg.h
api_name:
 - OFNOTIFYEX
 - OFNOTIFYEXA
 - OFNOTIFYEXW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _OFNOTIFYEXA structure


## -description


Contains information about a <a href="https://msdn.microsoft.com/en-us/library/ms646862(v=VS.85).aspx">CDN_INCLUDEITEM</a> notification message. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification message being sent. 


### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a> structure containing the values specified when the <b>Open</b> or <b>Save As</b> dialog box was created. 


### -field psf

Type: <b>LPVOID</b>

A pointer to the  interface for the folder or shell name-space extension whose items are being enumerated. 


### -field pidl

Type: <b>LPVOID</b>

A pointer to an item identifier list that identifies an item in the container identified by the <b>psf</b> member. The item identifier is relative to the <b>psf</b> container. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646862(v=VS.85).aspx">CDN_INCLUDEITEM</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646931(v=VS.85).aspx">OFNHookProc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646836(v=VS.85).aspx">OFNOTIFY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646839(v=VS.85).aspx">OPENFILENAME</a>



<b>Reference</b>
 

 

