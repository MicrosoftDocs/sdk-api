---
UID: NS:richedit._msgfilter
title: MSGFILTER (richedit.h)
description: Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an EN_MSGFILTER notification code, enabling the parent to change the message or prevent it from being processed.
helpviewer_keywords: ["MSGFILTER","MSGFILTER structure [Windows Controls]","_win32_MSGFILTER_str","_win32_MSGFILTER_str_cpp","controls.MSGFILTER","controls._win32_MSGFILTER_str","richedit/MSGFILTER"]
old-location: controls\MSGFILTER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\msgfilter.htm
ms.date: 12/05/2018
ms.keywords: MSGFILTER, MSGFILTER structure [Windows Controls], _win32_MSGFILTER_str, _win32_MSGFILTER_str_cpp, controls.MSGFILTER, controls._win32_MSGFILTER_str, richedit/MSGFILTER
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
req.typenames: MSGFILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _msgfilter
 - richedit/_msgfilter
 - MSGFILTER
 - richedit/MSGFILTER
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
 - MSGFILTER
---

# MSGFILTER structure


## -description

Contains information about a keyboard or mouse event. A rich edit control sends this structure to its parent window as part of an <a href="/windows/win32/controls/en-msgfilter">EN_MSGFILTER</a> notification code, enabling the parent to change the message or prevent it from being processed.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

The <b>code</b> member of the <a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure is the <a href="/windows/win32/controls/en-msgfilter">EN_MSGFILTER</a> notification code that identifies the message being sent.

### -field msg

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Keyboard or mouse message identifier.

### -field wParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

The 
					<b>wParam</b> parameter of the message.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The 
					<b>lParam</b> parameter of the message.

## -see-also

<a href="/windows/win32/controls/en-msgfilter">EN_MSGFILTER</a>
