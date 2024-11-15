---
UID: NS:richedit._enlink
title: ENLINK (richedit.h)
description: Contains information about an EN_LINK notification code from a rich edit control.
helpviewer_keywords: ["ENLINK","ENLINK structure [Windows Controls]","_win32_ENLINK_str","_win32_ENLINK_str_cpp","controls.ENLINK","controls._win32_ENLINK_str","richedit/ENLINK"]
old-location: controls\ENLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enlink.htm
ms.date: 12/05/2018
ms.keywords: ENLINK, ENLINK structure [Windows Controls], _win32_ENLINK_str, _win32_ENLINK_str_cpp, controls.ENLINK, controls._win32_ENLINK_str, richedit/ENLINK
req.header: richedit.h
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
req.typenames: ENLINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _enlink
 - richedit/_enlink
 - ENLINK
 - richedit/ENLINK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - ENLINK
---

# ENLINK structure


## -description

Contains information about an <a href="/windows/win32/controls/en-link">EN_LINK</a> notification code from a rich edit control.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

The code member of this structure identifies the notification code being sent.

### -field msg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifier of the message that caused the rich edit control to send the <a href="/windows/win32/controls/en-link">EN_LINK</a> notification code.

### -field wParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

The <b>wParam</b> parameter of the message received by the rich edit control.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The <b>lParam</b> parameter of the message received by the rich edit control.

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The range of consecutive characters in the rich edit control that have the CFE_LINK effect.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a>



<a href="/windows/win32/controls/en-link">EN_LINK</a>



<a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a>



<b>Reference</b>
