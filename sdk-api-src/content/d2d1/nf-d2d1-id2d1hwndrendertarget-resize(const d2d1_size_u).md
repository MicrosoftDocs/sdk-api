---
UID: NF:d2d1.ID2D1HwndRenderTarget.Resize(const D2D1_SIZE_U)
title: ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U)
author: windows-sdk-content
description: Changes the size of the render target to the specified pixel size.
old-location: direct2d\ID2D1HwndRenderTarget_Resize_ptr_D2D_SIZE_U.htm
tech.root: direct2d
ms.assetid: 1a1e7aae-9660-4c35-9d7b-374f3ff28253
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID2D1HwndRenderTarget interface [Direct2D],Resize method, ID2D1HwndRenderTarget.Resize, ID2D1HwndRenderTarget.Resize(const D2D1_SIZE_U), ID2D1HwndRenderTarget::Resize, ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U), Resize, Resize method [Direct2D], Resize method [Direct2D],ID2D1HwndRenderTarget interface, d2d1/ID2D1HwndRenderTarget::Resize, direct2d.ID2D1HwndRenderTarget_Resize_ptr_D2D_SIZE_U
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
 - ID2D1HwndRenderTarget.Resize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U)


## -description


Changes the size of the render target to the specified pixel size.


## -parameters




### -param pixelSize [in]

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a>*</b>

The new size of the render target in device pixels.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After this method is called, the contents of the render target's back-buffer are not defined, even if the <a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS</a> option was specified when the render target was created.




## -see-also




<a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>
 

 

