---
UID: NF:vfw.MCIWndSaveDialog
title: MCIWndSaveDialog macro (vfw.h)
description: The MCIWndSaveDialog macro saves the content currently used by an MCI device. This macro displays the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the MCI_SAVE command.
helpviewer_keywords: ["MCIWndSaveDialog","MCIWndSaveDialog macro [Windows Multimedia]","_win32_MCIWndSaveDialog","multimedia.mciwndsavedialog","vfw/MCIWndSaveDialog"]
old-location: multimedia\mciwndsavedialog.htm
tech.root: Multimedia
ms.assetid: 3ab1121f-5122-424b-a1df-ceeb57751dac
ms.date: 07/01/2025
ms.keywords: MCIWndSaveDialog, MCIWndSaveDialog macro [Windows Multimedia], _win32_MCIWndSaveDialog, multimedia.mciwndsavedialog, vfw/MCIWndSaveDialog
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
 - MCIWndSaveDialog
 - vfw/MCIWndSaveDialog
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
 - MCIWndSaveDialog
---

# MCIWndSaveDialog macro

## -syntax

```cpp
LONG MCIWndSaveDialog(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndSaveDialog</b> macro saves the content currently used by an MCI device. This macro displays the Save dialog box to let the user select a filename to store the content. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-save">MCI_SAVE</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.
