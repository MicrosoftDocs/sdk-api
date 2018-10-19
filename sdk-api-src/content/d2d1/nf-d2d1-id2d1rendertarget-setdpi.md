---
UID: NF:d2d1.ID2D1RenderTarget.SetDpi
title: ID2D1RenderTarget::SetDpi
author: windows-sdk-content
description: Sets the dots per inch (DPI) of the render target.
old-location: direct2d\ID2D1RenderTarget_SetDpi.htm
tech.root: direct2d
ms.assetid: 603a838b-4abc-4adf-93a9-ec8535d42ed6
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetDpi method, ID2D1RenderTarget.SetDpi, ID2D1RenderTarget::SetDpi, SetDpi, SetDpi method [Direct2D], SetDpi method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetDpi, direct2d.ID2D1RenderTarget_SetDpi
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
 - ID2D1RenderTarget.SetDpi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::SetDpi


## -description


Sets the dots per inch (DPI) of the render target. 


## -parameters




### -param dpiX

Type: <b>FLOAT</b>

A value greater than or equal to zero that specifies the horizontal DPI of the render target.


### -param dpiY

Type: <b>FLOAT</b>

A value greater than or equal to zero that specifies the vertical DPI of the render target.


## -returns



This method does not return a value.




## -remarks



This method specifies the mapping from pixel space to device-independent space  for the render target.  If both <i>dpiX</i> and <i>dpiY</i> are 0, the factory-read system DPI is chosen. If one parameter is zero and the other unspecified, the DPI is not changed.

For <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, the DPI defaults to the most recently factory-read system DPI. The default value for all other render targets is 96 DPI.  




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

