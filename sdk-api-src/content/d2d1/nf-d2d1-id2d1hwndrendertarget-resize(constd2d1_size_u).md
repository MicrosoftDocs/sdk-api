---
UID: NF:d2d1.ID2D1HwndRenderTarget.Resize(const D2D1_SIZE_U)
title: ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U) (d2d1.h)
description: Changes the size of the render target to the specified pixel size.helpviewer_keywords: ["ID2D1HwndRenderTarget interface [Direct2D]","Resize method","ID2D1HwndRenderTarget.Resize","ID2D1HwndRenderTarget.Resize(const D2D1_SIZE_U)","ID2D1HwndRenderTarget::Resize","ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U)","Resize","Resize method [Direct2D]","Resize method [Direct2D]","ID2D1HwndRenderTarget interface","d2d1/ID2D1HwndRenderTarget::Resize","direct2d.ID2D1HwndRenderTarget_Resize_ptr_D2D_SIZE_U"]
old-location: direct2d\ID2D1HwndRenderTarget_Resize_ptr_D2D_SIZE_U.htm
tech.root: Direct2D
ms.assetid: 1a1e7aae-9660-4c35-9d7b-374f3ff28253
ms.date: 12/05/2018
ms.keywords: ID2D1HwndRenderTarget interface [Direct2D],Resize method, ID2D1HwndRenderTarget.Resize, ID2D1HwndRenderTarget.Resize(const D2D1_SIZE_U), ID2D1HwndRenderTarget::Resize, ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U), Resize, Resize method [Direct2D], Resize method [Direct2D],ID2D1HwndRenderTarget interface, d2d1/ID2D1HwndRenderTarget::Resize, direct2d.ID2D1HwndRenderTarget_Resize_ptr_D2D_SIZE_U
f1_keywords:
- d2d1/ID2D1HwndRenderTarget.Resize
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1HwndRenderTarget::Resize(const D2D1_SIZE_U)


## -description


Changes the size of the render target to the specified pixel size.


## -parameters




### -param pixelSize [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/Direct2D/d2d1-size-u">D2D1_SIZE_U</a>*</b>

The new size of the render target in device pixels.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After this method is called, the contents of the render target's back-buffer are not defined, even if the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options">D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS</a> option was specified when the render target was created.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>
 

 

