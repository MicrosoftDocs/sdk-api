---
UID: NS:commctrl.tagNMTBSAVE
title: NMTBSAVE (commctrl.h)
description: This structure is passed to applications when they receive a TBN_SAVE notification code. It contains information about the button currently being saved. Applications can modify the values of the members to save additional information.
helpviewer_keywords: ["*LPNMTBSAVE","LPNMTBSAVE","LPNMTBSAVE structure pointer [Windows Controls]","NMTBSAVE","NMTBSAVE structure [Windows Controls]","_win32_NMTBSAVE","_win32_NMTBSAVE_cpp","commctrl/LPNMTBSAVE","commctrl/NMTBSAVE","controls.NMTBSAVE","controls._win32_NMTBSAVE"]
old-location: controls\NMTBSAVE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtbsave.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTBSAVE, LPNMTBSAVE, LPNMTBSAVE structure pointer [Windows Controls], NMTBSAVE, NMTBSAVE structure [Windows Controls], _win32_NMTBSAVE, _win32_NMTBSAVE_cpp, commctrl/LPNMTBSAVE, commctrl/NMTBSAVE, controls.NMTBSAVE, controls._win32_NMTBSAVE'
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
targetos: Windows
req.typenames: NMTBSAVE, *LPNMTBSAVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTBSAVE
 - commctrl/tagNMTBSAVE
 - LPNMTBSAVE
 - commctrl/LPNMTBSAVE
 - NMTBSAVE
 - commctrl/NMTBSAVE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMTBSAVE
---

# NMTBSAVE structure


## -description

This structure is passed to applications when they receive a <a href="/windows/desktop/Controls/tbn-save">TBN_SAVE</a> notification code. It contains information about the button currently being saved. Applications can modify the values of the members to save additional information.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field pData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

A pointer to the data stream used to store the save information. When complete, it will contain blocks of Shell-defined information for each button, alternating with blocks defined by the application. Applications may also choose to place a block of global data at the start of 
					<b>pData</b>. The format and length of the application-defined blocks are determined by the application. When the save starts, the Shell will pass the amount of memory it needs in 
					<b>cbData</b>, but no memory will be allocated. You must allocate enough memory for 
					<b>pData</b> to hold your data, plus the Shell's.

### -field pCurrent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

A pointer to the start of the unused portion of the data stream. You should load your data here, and then advance 
					<b>pCurrent</b> to the start of the remaining unused portion. The Shell will then load the information for the next button, advance 
					<b>pCurrent</b>, and so on.

### -field cbData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the data stream. When the save starts, 
					<b>cbData</b> will be set to the amount of data needed by the Shell. You should change it to the total amount allocated.

### -field iItem

Type: <b>int</b>

This parameter is usually the zero-based index of the button currently being saved. It is set to -1 to indicate that a save is starting.

### -field cButtons

Type: <b>int</b>

An estimate of the number of buttons. Because it is based on the size of the data stream, it may be incorrect. The client should update it as appropriate.

### -field tbButton

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a></b>

A <a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structure that contains information about the button currently being saved.