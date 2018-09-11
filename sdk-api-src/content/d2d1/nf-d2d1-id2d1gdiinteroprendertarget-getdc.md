---
UID: NF:d2d1.ID2D1GdiInteropRenderTarget.GetDC
title: ID2D1GdiInteropRenderTarget::GetDC
author: windows-sdk-content
description: Retrieves the device context associated with this render target.
old-location: direct2d\ID2D1GdiInteropRenderTarget_GetDC.htm
tech.root: direct2d
ms.assetid: 40797258-84a0-44ee-8b64-04ceb3eb1998
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDC, GetDC method [Direct2D], GetDC method [Direct2D],ID2D1GdiInteropRenderTarget interface, ID2D1GdiInteropRenderTarget interface [Direct2D],GetDC method, ID2D1GdiInteropRenderTarget.GetDC, ID2D1GdiInteropRenderTarget::GetDC, d2d1/ID2D1GdiInteropRenderTarget::GetDC, direct2d.ID2D1GdiInteropRenderTarget_GetDC
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
 - ID2D1GdiInteropRenderTarget.GetDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GdiInteropRenderTarget::GetDC


## -description


Retrieves the device context associated with this render target.


## -parameters




### -param mode

Type: <b><a href="https://msdn.microsoft.com/a7837fe4-6e11-42a0-8a85-cba42e0f123a">D2D1_DC_INITIALIZE_MODE</a></b>

A value that specifies whether the device context should be cleared.


### -param hdc [out]

Type: <b>HDC*</b>

When this method returns, contains the device context associated with this render target. You must allocate storage for this parameter.  


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method flushes the render target.

This command can be called only after <a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a> and before <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>. 

<div class="alert"><b>Note</b>  In Windows 7 and earlier, you should not call <b>GetDC</b> between <a href="https://msdn.microsoft.com/db2e975e-e5c5-4c57-8071-ec042b9a6fb9">PushAxisAlignedClip</a>/<a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> commands or between <a href="https://msdn.microsoft.com/0fc7ac38-ff74-4f3b-9aa2-025a99e6b013">PushLayer</a>/<a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>.  However, this restriction does not apply to Windows 8 and later.</div>
<div> </div>

<a href="https://msdn.microsoft.com/802bd023-f223-4505-9911-95b43f3490e3">ReleaseDC</a> must be called once for each call to <b>GetDC</b>.




## -see-also




<a href="https://msdn.microsoft.com/cb992ddd-21b2-4eba-b7c4-e391bdd23a9d">ID2D1GdiInteropRenderTarget</a>
 

 

