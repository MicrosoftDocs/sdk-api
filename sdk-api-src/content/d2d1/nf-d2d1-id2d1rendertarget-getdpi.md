---
UID: NF:d2d1.ID2D1RenderTarget.GetDpi
title: ID2D1RenderTarget::GetDpi
author: windows-sdk-content
description: Return the render target's dots per inch (DPI).
old-location: direct2d\ID2D1RenderTarget_GetDpi.htm
tech.root: direct2d
ms.assetid: 72a25b78-96fd-42bf-9e71-6bb80efea0ac
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetDpi method, ID2D1RenderTarget.GetDpi, ID2D1RenderTarget::GetDpi, d2d1/ID2D1RenderTarget::GetDpi, direct2d.ID2D1RenderTarget_GetDpi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
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
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.GetDpi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::GetDpi


## -description


Return the render target's dots per inch (DPI).


## -parameters




### -param dpiX [out]

Type: <b>FLOAT*</b>

When this method returns, contains the horizontal DPI of the render target. This parameter is passed uninitialized.


### -param dpiY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the vertical DPI of the render target. This parameter is passed uninitialized.


## -returns



This method does not return a value.




## -remarks



This method indicates the mapping from pixel space to device-independent space  for the render target.  

For <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, the DPI defaults to the most recently factory-read system DPI. The default value for all other render targets is 96 DPI.  




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

