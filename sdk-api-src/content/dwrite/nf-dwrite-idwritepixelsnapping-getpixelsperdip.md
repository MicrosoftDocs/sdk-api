---
UID: NF:dwrite.IDWritePixelSnapping.GetPixelsPerDip
title: IDWritePixelSnapping::GetPixelsPerDip (dwrite.h)
description: Gets the number of physical pixels per DIP.
helpviewer_keywords: ["GetPixelsPerDip","GetPixelsPerDip method [Direct Write]","GetPixelsPerDip method [Direct Write]","IDWritePixelSnapping interface","IDWritePixelSnapping interface [Direct Write]","GetPixelsPerDip method","IDWritePixelSnapping.GetPixelsPerDip","IDWritePixelSnapping::GetPixelsPerDip","directwrite.IDWritePixelSnapping_GetPixelsPerDip","dwrite/IDWritePixelSnapping::GetPixelsPerDip"]
old-location: directwrite\IDWritePixelSnapping_GetPixelsPerDip.htm
tech.root: DirectWrite
ms.assetid: 41b07197-e50c-4145-a931-e35e778541cc
ms.date: 12/05/2018
ms.keywords: GetPixelsPerDip, GetPixelsPerDip method [Direct Write], GetPixelsPerDip method [Direct Write],IDWritePixelSnapping interface, IDWritePixelSnapping interface [Direct Write],GetPixelsPerDip method, IDWritePixelSnapping.GetPixelsPerDip, IDWritePixelSnapping::GetPixelsPerDip, directwrite.IDWritePixelSnapping_GetPixelsPerDip, dwrite/IDWritePixelSnapping::GetPixelsPerDip
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWritePixelSnapping::GetPixelsPerDip
 - dwrite/IDWritePixelSnapping::GetPixelsPerDip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWritePixelSnapping.GetPixelsPerDip
---

# IDWritePixelSnapping::GetPixelsPerDip


## -description

 Gets the number of physical pixels per DIP.

## -parameters

### -param clientDrawingContext

Type: <b>void*</b>

The drawing context passed to <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a>.

### -param pixelsPerDip [out]

Type: <b>FLOAT*</b>

When this method returns, contains the number of physical pixels per DIP.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Because a DIP (device-independent pixel) is 1/96 inch, 
      the <i>pixelsPerDip</i> value is the number of logical pixels per inch divided by 96.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping">IDWritePixelSnapping</a>

