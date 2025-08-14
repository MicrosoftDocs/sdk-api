---
UID: NF:vfw.MCIWndStep
title: MCIWndStep macro (vfw.h)
description: The MCIWndStep macro moves the current position in the content forward or backward by a specified increment. You can use this macro or explicitly send the MCI_STEP command.
helpviewer_keywords: ["MCIWndStep","MCIWndStep macro [Windows Multimedia]","_win32_MCIWndStep","multimedia.mciwndstep","vfw/MCIWndStep"]
old-location: multimedia\mciwndstep.htm
tech.root: Multimedia
ms.assetid: 4490901c-a58c-465c-a7b3-230456848da3
ms.date: 07/01/2025
ms.keywords: MCIWndStep, MCIWndStep macro [Windows Multimedia], _win32_MCIWndStep, multimedia.mciwndstep, vfw/MCIWndStep
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
 - MCIWndStep
 - vfw/MCIWndStep
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
 - MCIWndStep
---

# MCIWndStep macro

## -syntax

```cpp
LONG MCIWndStep(
     hwnd,
     n
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndStep</b> macro moves the current position in the content forward or backward by a specified increment. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mci-step">MCI_STEP</a> command.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param n

Step value. Negative values step the device through the content in reverse. The units for the step value depend on the current time format.
