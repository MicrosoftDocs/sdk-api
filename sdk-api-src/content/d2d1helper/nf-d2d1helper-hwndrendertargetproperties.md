---
UID: NF:d2d1helper.HwndRenderTargetProperties
title: HwndRenderTargetProperties function (d2d1helper.h)
author: windows-sdk-content
description: Creates a D2D1_HWND_RENDER_TARGET_PROPERTIES structure.
old-location: direct2d\hwndrendertargetproperties.htm
tech.root: Direct2D
ms.assetid: 41d4c58d-6840-48b6-8e31-1a0c412156cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HwndRenderTargetProperties, HwndRenderTargetProperties function [Direct2D], d2d1helper/HwndRenderTargetProperties, direct2d.hwndrendertargetproperties
ms.topic: function
req.header: d2d1helper.h
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
 - HwndRenderTargetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HwndRenderTargetProperties function


## -description


Creates a <a href="https://msdn.microsoft.com/4300843a-a24f-4f9e-a396-67172f083638">D2D1_HWND_RENDER_TARGET_PROPERTIES</a> structure.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The HWND to which the render target issues the output from its drawing commands. 


### -param pixelSize [in]

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The size of the render target, in pixels. The default value is a <a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a> that has a width and height of 0.


### -param presentOptions [in]

Type: <b><a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS</a></b>

A value that specifies whether the render target retains the frame after it is presented and whether the render target waits for the device to refresh before presenting. The default value is <a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS_NONE</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4300843a-a24f-4f9e-a396-67172f083638">D2D1_HWND_RENDER_TARGET_PROPERTIES</a></b>

A structure that contains the HWND, pixel size, and presentation options for an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>.



