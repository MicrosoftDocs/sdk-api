---
UID: NF:vfw.MCIWndOpenDialog
title: MCIWndOpenDialog macro (vfw.h)
description: The MCIWndOpenDialog macro opens a user-specified data file and corresponding type of MCI device, and associates them with an MCIWnd window.
helpviewer_keywords: ["MCIWndOpenDialog","MCIWndOpenDialog macro [Windows Multimedia]","_win32_MCIWndOpenDialog","multimedia.mciwndopendialog","vfw/MCIWndOpenDialog"]
old-location: multimedia\mciwndopendialog.htm
tech.root: Multimedia
ms.assetid: 28110649-24a8-45c5-bf1a-b05a6476d9a5
ms.date: 07/01/2025
ms.keywords: MCIWndOpenDialog, MCIWndOpenDialog macro [Windows Multimedia], _win32_MCIWndOpenDialog, multimedia.mciwndopendialog, vfw/MCIWndOpenDialog
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
 - MCIWndOpenDialog
 - vfw/MCIWndOpenDialog
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
 - MCIWndOpenDialog
---

# MCIWndOpenDialog macro

## -syntax

```cpp
LONG MCIWndOpenDialog(
     hwnd
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndOpenDialog</b> macro opens a user-specified data file and corresponding type of MCI device, and associates them with an MCIWnd window. This macro displays the Open dialog box for the user to select the data file to associate with an MCI window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-open">MCIWNDM_OPEN</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.
