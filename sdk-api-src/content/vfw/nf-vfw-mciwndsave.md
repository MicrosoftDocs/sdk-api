---
UID: NF:vfw.MCIWndSave
title: MCIWndSave macro (vfw.h)
description: The MCIWndSave macro saves the content currently used by an MCI device.
helpviewer_keywords: ["MCIWndSave","MCIWndSave macro [Windows Multimedia]","_win32_MCIWndSave","multimedia.mciwndsave","vfw/MCIWndSave"]
old-location: multimedia\mciwndsave.htm
tech.root: Multimedia
ms.assetid: 11b67381-5177-4b55-b0a2-a633e60ae571
ms.date: 07/01/2025
ms.keywords: MCIWndSave, MCIWndSave macro [Windows Multimedia], _win32_MCIWndSave, multimedia.mciwndsave, vfw/MCIWndSave
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndSave
 - vfw/MCIWndSave
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndSave
---

# MCIWndSave macro

## -syntax

```cpp
LONG MCIWndSave(
     hwnd,
     szFile
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndSave</b> macro saves the content currently used by an MCI device. This macro can save the content to a specified data file or display the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-save">MCI_SAVE</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param szFile

Null-terminated string containing the name and path of the destination file. Specify −1 for this parameter to display the Save dialog box.
