---
UID: NF:d2d1.ID2D1GdiInteropRenderTarget.ReleaseDC
title: ID2D1GdiInteropRenderTarget::ReleaseDC
author: windows-sdk-content
description: Indicates that drawing with the device context retrieved using the GetDC method is finished.
old-location: direct2d\ID2D1GdiInteropRenderTarget_ReleaseDC.htm
tech.root: Direct2D
ms.assetid: 802bd023-f223-4505-9911-95b43f3490e3
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1GdiInteropRenderTarget interface [Direct2D],ReleaseDC method, ID2D1GdiInteropRenderTarget.ReleaseDC, ID2D1GdiInteropRenderTarget::ReleaseDC, ReleaseDC, ReleaseDC method [Direct2D], ReleaseDC method [Direct2D],ID2D1GdiInteropRenderTarget interface, d2d1/ID2D1GdiInteropRenderTarget::ReleaseDC, direct2d.ID2D1GdiInteropRenderTarget_ReleaseDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - ID2D1GdiInteropRenderTarget.ReleaseDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GdiInteropRenderTarget::ReleaseDC


## -description


Indicates that drawing with the device context retrieved using the <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">GetDC</a> method is finished. 


## -parameters




### -param update [in, optional]

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The modified region of the device context, or <b>NULL</b> to specify the entire render target. 


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>ReleaseDC</b> must be called once for each call to <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">GetDC</a>.




## -see-also




<a href="https://msdn.microsoft.com/cb992ddd-21b2-4eba-b7c4-e391bdd23a9d">ID2D1GdiInteropRenderTarget</a>
 

 

