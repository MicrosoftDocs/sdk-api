---
UID: NS:commctrl.tagNMTOOLBARA
title: NMTOOLBARA (commctrl.h)
description: Contains information used to process toolbar notification codes. This structure supersedes the TBNOTIFY structure. (ANSI)
helpviewer_keywords: ["*LPNMTOOLBARA","LPNMTOOLBAR","LPNMTOOLBAR structure pointer [Windows Controls]","NMTOOLBAR","NMTOOLBAR structure [Windows Controls]","NMTOOLBARA","NMTOOLBARW","_win32_NMTOOLBAR","_win32_NMTOOLBAR_cpp","commctrl/LPNMTOOLBAR","commctrl/NMTOOLBAR","commctrl/NMTOOLBARA","commctrl/NMTOOLBARW","controls.NMTOOLBAR","controls._win32_NMTOOLBAR"]
old-location: controls\NMTOOLBAR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\nmtoolbar.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTOOLBARA, LPNMTOOLBAR, LPNMTOOLBAR structure pointer [Windows Controls], NMTOOLBAR, NMTOOLBAR structure [Windows Controls], NMTOOLBARA, NMTOOLBARW, _win32_NMTOOLBAR, _win32_NMTOOLBAR_cpp, commctrl/LPNMTOOLBAR, commctrl/NMTOOLBAR, commctrl/NMTOOLBARA, commctrl/NMTOOLBARW, controls.NMTOOLBAR, controls._win32_NMTOOLBAR'
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
targetos: Windows
req.typenames: NMTOOLBARA, *LPNMTOOLBARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMTOOLBARA
 - commctrl/tagNMTOOLBARA
 - LPNMTOOLBARA
 - commctrl/LPNMTOOLBARA
 - NMTOOLBARA
 - commctrl/NMTOOLBARA
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
 - NMTOOLBAR
 - NMTOOLBARA
 - NMTOOLBARW
---

# NMTOOLBARA structure


## -description

Contains information used to process toolbar notification codes. This structure supersedes the 
			<b>TBNOTIFY</b> structure.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field iItem

Type: <b>int</b>

Command identifier of the button associated with the notification code.

### -field tbButton

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structure that contains information about the toolbar button associated with the notification code. This member only contains valid information with the <a href="/windows/desktop/Controls/tbn-queryinsert">TBN_QUERYINSERT</a> and <a href="/windows/desktop/Controls/tbn-querydelete">TBN_QUERYDELETE</a> notification codes.

### -field cchText

Type: <b>int</b>

Count of characters in the button text.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a character buffer that contains the button text.

### -field rcButton

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the area covered by the button.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMTOOLBAR as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
