---
UID: NS:commctrl.tagNMTOOLBARW
title: tagNMTOOLBARW
author: windows-sdk-content
description: Contains information used to process toolbar notification codes. This structure supersedes the TBNOTIFY structure.
old-location: controls\NMTOOLBAR.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtoolbar.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPNMTOOLBARW, LPNMTOOLBAR, LPNMTOOLBAR structure pointer [Windows Controls], NMTOOLBAR, NMTOOLBAR structure [Windows Controls], NMTOOLBARA, NMTOOLBARW, _win32_NMTOOLBAR, _win32_NMTOOLBAR_cpp, commctrl/LPNMTOOLBAR, commctrl/NMTOOLBAR, commctrl/NMTOOLBARA, commctrl/NMTOOLBARW, controls.NMTOOLBAR, controls._win32_NMTOOLBAR, tagNMTOOLBARW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTOOLBARW (Unicode) and NMTOOLBARA (ANSI)
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
 - Commctrl.h
api_name:
 - NMTOOLBAR
 - NMTOOLBARA
 - NMTOOLBARW
product: Windows
targetos: Windows
req.typenames: NMTOOLBARW, *LPNMTOOLBARW
req.redist: 
---

# tagNMTOOLBARW structure


## -description


Contains information used to process toolbar notification codes. This structure supersedes the 
			<b>TBNOTIFY</b> structure. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field iItem

Type: <b>int</b>

Command identifier of the button associated with the notification code. 


### -field tbButton

Type: <b><a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a></b>


<a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structure that contains information about the toolbar button associated with the notification code. This member only contains valid information with the <a href="https://msdn.microsoft.com/d389fabb-16f6-43aa-a4b6-abb80723345b">TBN_QUERYINSERT</a> and <a href="https://msdn.microsoft.com/fa6a8fe4-a9a3-4c59-9237-d28bd34d664c">TBN_QUERYDELETE</a> notification codes. 


### -field cchText

Type: <b>int</b>

Count of characters in the button text. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Address of a character buffer that contains the button text. 


### -field rcButton

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 5.80.</a> A <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that defines the area covered by the button. 

