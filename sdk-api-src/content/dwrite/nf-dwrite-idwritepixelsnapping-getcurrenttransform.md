---
UID: NF:dwrite.IDWritePixelSnapping.GetCurrentTransform
title: IDWritePixelSnapping::GetCurrentTransform (dwrite.h)
author: windows-sdk-content
description: Gets a transform that maps abstract coordinates to DIPs.
old-location: directwrite\IDWritePixelSnapping_GetCurrentTransform.htm
tech.root: DirectWrite
ms.assetid: d3cfbea6-c240-47e9-a072-a59626e39ee9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentTransform, GetCurrentTransform method [Direct Write], GetCurrentTransform method [Direct Write],IDWritePixelSnapping interface, IDWritePixelSnapping interface [Direct Write],GetCurrentTransform method, IDWritePixelSnapping.GetCurrentTransform, IDWritePixelSnapping::GetCurrentTransform, directwrite.IDWritePixelSnapping_GetCurrentTransform, dwrite/IDWritePixelSnapping::GetCurrentTransform
ms.topic: method
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWritePixelSnapping.GetCurrentTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWritePixelSnapping::GetCurrentTransform


## -description


 Gets a transform that maps abstract coordinates to DIPs.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The drawing context passed to <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a>.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

When this method returns, contains a structure which has transform information for  pixel snapping.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b1b1eeb7-934f-42f4-ac01-50973a94996e">IDWritePixelSnapping</a>
 

 

