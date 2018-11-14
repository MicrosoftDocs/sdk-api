---
UID: NS:commctrl.tagNMTBSAVE
title: tagNMTBSAVE
author: windows-sdk-content
description: This structure is passed to applications when they receive a TBN_SAVE notification code. It contains information about the button currently being saved. Applications can modify the values of the members to save additional information.
old-location: controls\NMTBSAVE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbsave.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMTBSAVE, LPNMTBSAVE, LPNMTBSAVE structure pointer [Windows Controls], NMTBSAVE, NMTBSAVE structure [Windows Controls], _win32_NMTBSAVE, _win32_NMTBSAVE_cpp, commctrl/LPNMTBSAVE, commctrl/NMTBSAVE, controls.NMTBSAVE, controls._win32_NMTBSAVE, tagNMTBSAVE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Commctrl.h
api_name:
 - NMTBSAVE
product: Windows
targetos: Windows
req.typenames: NMTBSAVE, *LPNMTBSAVE
req.redist: 
---

# tagNMTBSAVE structure


## -description


This structure is passed to applications when they receive a <a href="https://msdn.microsoft.com/31622f5e-2e33-4a42-8c49-cc3028a6fa62">TBN_SAVE</a> notification code. It contains information about the button currently being saved. Applications can modify the values of the members to save additional information. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field pData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

A pointer to the data stream used to store the save information. When complete, it will contain blocks of Shell-defined information for each button, alternating with blocks defined by the application. Applications may also choose to place a block of global data at the start of 
					<b>pData</b>. The format and length of the application-defined blocks are determined by the application. When the save starts, the Shell will pass the amount of memory it needs in 
					<b>cbData</b>, but no memory will be allocated. You must allocate enough memory for 
					<b>pData</b> to hold your data, plus the Shell's. 


### -field pCurrent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

A pointer to the start of the unused portion of the data stream. You should load your data here, and then advance 
					<b>pCurrent</b> to the start of the remaining unused portion. The Shell will then load the information for the next button, advance 
					<b>pCurrent</b>, and so on. 


### -field cbData

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of the data stream. When the save starts, 
					<b>cbData</b> will be set to the amount of data needed by the Shell. You should change it to the total amount allocated. 


### -field iItem

Type: <b>int</b>

This parameter is usually the zero-based index of the button currently being saved. It is set to -1 to indicate that a save is starting. 


### -field cButtons

Type: <b>int</b>

An estimate of the number of buttons. Because it is based on the size of the data stream, it may be incorrect. The client should update it as appropriate. 


### -field tbButton

Type: <b><a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a></b>

A <a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structure that contains information about the button currently being saved. 

