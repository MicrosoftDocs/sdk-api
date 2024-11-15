---
UID: NS:richedit._reqresize
title: REQRESIZE (richedit.h)
description: Contains the requested size of a rich edit control. A rich edit control sends this structure to its parent window as part of an EN_REQUESTRESIZE notification code.
helpviewer_keywords: ["REQRESIZE","REQRESIZE structure [Windows Controls]","_win32_REQRESIZE_str","_win32_REQRESIZE_str_cpp","controls.REQRESIZE","controls._win32_REQRESIZE_str","richedit/REQRESIZE"]
old-location: controls\REQRESIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\reqresize.htm
ms.date: 12/05/2018
ms.keywords: REQRESIZE, REQRESIZE structure [Windows Controls], _win32_REQRESIZE_str, _win32_REQRESIZE_str_cpp, controls.REQRESIZE, controls._win32_REQRESIZE_str, richedit/REQRESIZE
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
req.typenames: REQRESIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _reqresize
 - richedit/_reqresize
 - REQRESIZE
 - richedit/REQRESIZE
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
 - REQRESIZE
---

# REQRESIZE structure


## -description

Contains the requested size of a rich edit control. A rich edit control sends this structure to its parent window as part of an <a href="/windows/win32/controls/en-requestresize">EN_REQUESTRESIZE</a> notification code.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

Notification header.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

Requested new size.

## -see-also

<a href="/windows/win32/controls/en-requestresize">EN_REQUESTRESIZE</a>

