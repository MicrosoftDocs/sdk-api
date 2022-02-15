---
UID: NF:dwrite.IDWriteTextLayout.HitTestPoint
title: IDWriteTextLayout::HitTestPoint (dwrite.h)
description: The application calls this function passing in a specific pixel location relative to the top-left location of the layout box and obtains the information about the correspondent hit-test metrics of the text string where the hit-test has occurred.
helpviewer_keywords: ["HitTestPoint","HitTestPoint method [Direct Write]","HitTestPoint method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","HitTestPoint method","IDWriteTextLayout.HitTestPoint","IDWriteTextLayout::HitTestPoint","directwrite.IDWriteTextLayout_HitTestPoint","dwrite/IDWriteTextLayout::HitTestPoint"]
old-location: directwrite\IDWriteTextLayout_HitTestPoint.htm
tech.root: DirectWrite
ms.assetid: 6eb10e03-beb6-4ad3-9b57-4b4be0e265de
ms.date: 12/05/2018
ms.keywords: HitTestPoint, HitTestPoint method [Direct Write], HitTestPoint method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],HitTestPoint method, IDWriteTextLayout.HitTestPoint, IDWriteTextLayout::HitTestPoint, directwrite.IDWriteTextLayout_HitTestPoint, dwrite/IDWriteTextLayout::HitTestPoint
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
 - IDWriteTextLayout::HitTestPoint
 - dwrite/IDWriteTextLayout::HitTestPoint
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
 - IDWriteTextLayout.HitTestPoint
---

# IDWriteTextLayout::HitTestPoint


## -description

 The application calls this function passing in a specific pixel location
     relative to the top-left location of the layout box and obtains the
     information about the correspondent hit-test metrics of the text string
     where the hit-test has occurred. When the specified pixel location is
     outside the text string, the function sets the output value <i>*isInside</i> to
     <b>FALSE</b>.

## -parameters

### -param pointX

Type: <b>FLOAT</b>

The pixel location X to hit-test, relative to the top-left location of the layout box.

### -param pointY

Type: <b>FLOAT</b>

The pixel location Y to hit-test, relative to the top-left location of the layout box.

### -param isTrailingHit [out]

Type: <b>BOOL*</b>

An output flag that indicates whether the hit-test location is at the leading or the trailing
         side of the character. When the output <i>*isInside</i> value is set to <b>FALSE</b>, this value is set according to the output
         <i>hitTestMetrics-&gt;textPosition</i> value to represent the edge closest to the hit-test location.

### -param isInside [out]

Type: <b>BOOL*</b>

An output flag that indicates whether the hit-test location is inside the text string.
         When <b>FALSE</b>, the position nearest the text's edge is returned.

### -param hitTestMetrics [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics">DWRITE_HIT_TEST_METRICS</a>*</b>

The output geometry fully enclosing the hit-test location. When the output <i>*isInside</i> value
         is set to <b>FALSE</b>, this structure represents the geometry enclosing the edge closest to the hit-test location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

