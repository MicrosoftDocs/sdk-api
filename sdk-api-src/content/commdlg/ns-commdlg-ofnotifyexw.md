---
UID: NS:commdlg._OFNOTIFYEXW
title: OFNOTIFYEXW (commdlg.h)
author: windows-sdk-content
description: Contains information about a CDN_INCLUDEITEM notification message.
old-location: dlgbox\ofnotifyex_str.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxstructures\ofnotifyex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPOFNOTIFYEXW, LPOFNOTIFYEX, LPOFNOTIFYEX structure pointer [Dialog Boxes], OFNOTIFYEX, OFNOTIFYEX structure [Dialog Boxes], OFNOTIFYEXA, OFNOTIFYEXW, _win32_OFNOTIFYEX_str, _win32_ofnotifyex_str_cpp, commdlg/LPOFNOTIFYEX, commdlg/OFNOTIFYEX, commdlg/OFNOTIFYEXA, commdlg/OFNOTIFYEXW, dlgbox.ofnotifyex_str, winui._win32_ofnotifyex_str"
ms.topic: struct
req.header: commdlg.h
req.include-header: Windows.h
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
 - OFNOTIFYEX
 - OFNOTIFYEXA
 - OFNOTIFYEXW
product: Windows
targetos: Windows
req.typenames: OFNOTIFYEXW, *LPOFNOTIFYEXW
req.redist: 
ms.custom: 19H1
---

# OFNOTIFYEXW structure


## -description


Contains information about a <a href="https://docs.microsoft.com/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a> notification message. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-_nmhdr">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification message being sent. 


### -field lpOFN

Type: <b>LPOPENFILENAME</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/commdlg/ns-commdlg-tagofna">OPENFILENAME</a> structure containing the values specified when the <b>Open</b> or <b>Save As</b> dialog box was created. 


### -field psf

Type: <b>LPVOID</b>

A pointer to the  interface for the folder or shell name-space extension whose items are being enumerated. 


### -field pidl

Type: <b>LPVOID</b>

A pointer to an item identifier list that identifies an item in the container identified by the <b>psf</b> member. The item identifier is relative to the <b>psf</b> container. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dlgbox/cdn-includeitem">CDN_INCLUDEITEM</a>



<a href="https://docs.microsoft.com/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nc-commdlg-lpofnhookproc">OFNHookProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/ns-commdlg-_ofnotifya">OFNOTIFY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/ns-commdlg-tagofna">OPENFILENAME</a>



<b>Reference</b>
 

 

