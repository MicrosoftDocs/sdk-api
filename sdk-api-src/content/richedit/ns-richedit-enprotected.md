---
UID: NS:richedit._enprotected
title: ENPROTECTED (richedit.h)
description: Contains information associated with an EN_PROTECTED notification code. A rich edit control sends this notification when the user attempts to edit protected text.
helpviewer_keywords: ["ENPROTECTED","ENPROTECTED structure [Windows Controls]","_win32_ENPROTECTED_str","_win32_ENPROTECTED_str_cpp","controls.ENPROTECTED","controls._win32_ENPROTECTED_str","richedit/ENPROTECTED"]
old-location: controls\ENPROTECTED.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enprotected.htm
ms.date: 12/05/2018
ms.keywords: ENPROTECTED, ENPROTECTED structure [Windows Controls], _win32_ENPROTECTED_str, _win32_ENPROTECTED_str_cpp, controls.ENPROTECTED, controls._win32_ENPROTECTED_str, richedit/ENPROTECTED
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
req.typenames: ENPROTECTED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _enprotected
 - richedit/_enprotected
 - ENPROTECTED
 - richedit/ENPROTECTED
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
 - ENPROTECTED
---

# ENPROTECTED structure


## -description

Contains information associated with an [EN_PROTECTED](/windows/win32/controls/en-protected) notification code. A rich edit control sends this notification when the user attempts to edit protected text.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a> notification header.

### -field msg

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

Message that triggered the notification.

### -field wParam

Type: <b><a href="/windows/win32/WinProg/windows-data-types">WPARAM</a></b>

The <b>wParam</b> parameter of the message.

### -field lParam

Type: <b><a href="/windows/win32/WinProg/windows-data-types">LPARAM</a></b>

The <b>lParam</b> parameter of the message.

### -field chrg

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-charrange">CHARRANGE</a></b>

The current selection.

## -see-also

[EN_PROTECTED](/windows/win32/controls/en-protected)
