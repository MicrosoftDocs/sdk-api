---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



