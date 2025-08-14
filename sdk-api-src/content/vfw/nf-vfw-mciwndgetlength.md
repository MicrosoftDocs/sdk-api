---
UID: NF:vfw.MCIWndGetLength
title: MCIWndGetLength macro (vfw.h)
description: The MCIWndGetLength macro retrieves the length of the content or file currently used by an MCI device. You can use this macro or explicitly send the MCIWNDM_GETLENGTH message.
helpviewer_keywords: ["MCIWndGetLength","MCIWndGetLength macro [Windows Multimedia]","_win32_MCIWndGetLength","multimedia.mciwndgetlength","vfw/MCIWndGetLength"]
old-location: multimedia\mciwndgetlength.htm
tech.root: Multimedia
ms.assetid: 2d027660-b2dd-4613-9583-30d7a45f7a1d
ms.date: 07/01/2025
ms.keywords: MCIWndGetLength, MCIWndGetLength macro [Windows Multimedia], _win32_MCIWndGetLength, multimedia.mciwndgetlength, vfw/MCIWndGetLength
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
 - MCIWndGetLength
 - vfw/MCIWndGetLength
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
 - MCIWndGetLength
---

# MCIWndGetLength macro

## -syntax

```cpp
UINT MCIWndGetLength(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the length. The units for the length depend on the current time format.


## -description

The <b>MCIWndGetLength</b> macro retrieves the length of the content or file currently used by an MCI device. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getlength">MCIWNDM_GETLENGTH</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -remarks

This value added to the value returned for the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndgetstart">MCIWndGetStart</a> macro equals the end of the content.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getlength">MCIWNDM_GETLENGTH</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mciwndgetstart">MCIWndGetStart</a>
