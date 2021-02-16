---
UID: NS:richedit._clipboardformat
title: CLIPBOARDFORMAT (richedit.h)
description: Specifies the clipboard format. This structure included with the EN_CLIPFORMAT notification.
helpviewer_keywords: ["CLIPBOARDFORMAT","CLIPBOARDFORMAT structure [Windows Controls]","controls.clipboardformat","richedit/CLIPBOARDFORMAT"]
old-location: controls\clipboardformat.htm
tech.root: Controls
ms.assetid: 5AD870B6-C4F1-446C-A516-171B24355EFA
ms.date: 12/05/2018
ms.keywords: CLIPBOARDFORMAT, CLIPBOARDFORMAT structure [Windows Controls], controls.clipboardformat, richedit/CLIPBOARDFORMAT
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CLIPBOARDFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _clipboardformat
 - richedit/_clipboardformat
 - CLIPBOARDFORMAT
 - richedit/CLIPBOARDFORMAT
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
 - CLIPBOARDFORMAT
---

# CLIPBOARDFORMAT structure


## -description

Specifies the clipboard format. This structure included with the <a href="/windows/desktop/Controls/en-clipformat">EN_CLIPFORMAT</a> notification.

## -struct-fields

### -field nmhdr

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

Structure that contains information about this notification message.

### -field cf

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A clipboard format registered by a call to the <a href="/windows/win32/api/winuser/nf-winuser-registerclipboardformata">RegisterClipboardFormat</a> function.

## -see-also

<a href="/windows/desktop/Controls/en-clipformat">EN_CLIPFORMAT</a>
