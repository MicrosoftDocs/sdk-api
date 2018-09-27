---
UID: NF:d2d1_1helper.SetDpiCompensatedEffectInput
title: SetDpiCompensatedEffectInput function
author: windows-sdk-content
description: Sets a bitmap as an effect input, while inserting a DPI compensation effect to preserve visual appearance as the device context's DPI changes.
old-location: direct2d\setdpicompensatedeffectinput.htm
tech.root: direct2d
ms.assetid: B9E2C5F7-2E05-441D-A902-6473E0235659
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: SetDpiCompensatedEffectInput, SetDpiCompensatedEffectInput function [Direct2D], d2d1_1helper/SetDpiCompensatedEffectInput, direct2d.setdpicompensatedeffectinput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - SetDpiCompensatedEffectInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDpiCompensatedEffectInput function


## -description


Sets a bitmap as an effect input, while inserting a DPI compensation effect
    to preserve visual appearance as the device context's DPI changes.


## -parameters




### -param deviceContext [in]

Type: <b><a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>*</b>

The device context that is the creator of the effect.


### -param effect [in]

Type: <b><a href="https://msdn.microsoft.com/e90d1830-c356-48f1-ac7b-1d94c8c26569">ID2D1Effect</a>*</b>

The function sets the input of this effect.


### -param inputIndex

Type: <b>UINT32</b>

The index of the input to be set.


### -param inputBitmap [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The input bitmap.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh447004(v=VS.85).aspx">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode for the DPI compensation effect.


### -param borderMode

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn934220(v=VS.85).aspx">D2D1_BORDER_MODE</a></b>

The border mode for the DPI compensation effect.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



