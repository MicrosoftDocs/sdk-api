---
UID: NF:dwrite.IDWriteTextLayout.HitTestTextRange
title: IDWriteTextLayout::HitTestTextRange (dwrite.h)
description: The application calls this function to get a set of hit-test metrics corresponding to a range of text positions. One of the main usages is to implement highlight selection of the text string.
helpviewer_keywords: ["HitTestTextRange","HitTestTextRange method [Direct Write]","HitTestTextRange method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","HitTestTextRange method","IDWriteTextLayout.HitTestTextRange","IDWriteTextLayout::HitTestTextRange","directwrite.IDWriteTextLayout_HitTestTextRange","dwrite/IDWriteTextLayout::HitTestTextRange"]
old-location: directwrite\IDWriteTextLayout_HitTestTextRange.htm
tech.root: DirectWrite
ms.assetid: 970ea72c-d097-42c2-9d93-774387ba7881
ms.date: 12/05/2018
ms.keywords: HitTestTextRange, HitTestTextRange method [Direct Write], HitTestTextRange method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],HitTestTextRange method, IDWriteTextLayout.HitTestTextRange, IDWriteTextLayout::HitTestTextRange, directwrite.IDWriteTextLayout_HitTestTextRange, dwrite/IDWriteTextLayout::HitTestTextRange
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
 - IDWriteTextLayout::HitTestTextRange
 - dwrite/IDWriteTextLayout::HitTestTextRange
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
 - IDWriteTextLayout.HitTestTextRange
---

# IDWriteTextLayout::HitTestTextRange


## -description

 The application calls this function to get a set of hit-test metrics corresponding to a range of text positions. One of the main usages is to implement highlight selection of the text string. 

The function returns E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), when the buffer size of hitTestMetrics is too small to hold all the regions calculated by the function. In this situation, the function sets the output value *actualHitTestMetricsCount to the number of geometries calculated. 

The application is responsible for allocating a new buffer of greater size and calling the function again.

A good value to use as an initial value for maxHitTestMetricsCount may be calculated from the following equation:



``` syntax
maxHitTestMetricsCount = lineCount * maxBidiReorderingDepth
```



where lineCount is obtained from the value of the output argument
     *actualLineCount (from the function <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>::GetLineLengths),
     and the maxBidiReorderingDepth value from the <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics">DWRITE_TEXT_METRICS</a> structure of the output argument *textMetrics (from the function
     <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>::<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">CreateTextLayout</a>).

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The first text position of the specified range.

### -param textLength

Type: <b>UINT32</b>

The number of positions of the specified range.

### -param originX

Type: <b>FLOAT</b>

The origin pixel location X at the left of the layout box. This offset is added to the hit-test metrics returned.

### -param originY

Type: <b>FLOAT</b>

The origin pixel location Y at the top of the layout box. This offset is added to the hit-test metrics returned.

### -param hitTestMetrics [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics">DWRITE_HIT_TEST_METRICS</a>*</b>

When this method returns, contains a pointer to a buffer of the output geometry fully enclosing the specified position range.  The buffer must be at least as large as <i>maxHitTestMetricsCount</i>.

### -param maxHitTestMetricsCount

Type: <b>UINT32</b>

Maximum number of boxes <i>hitTestMetrics</i> could hold in its buffer memory.

### -param actualHitTestMetricsCount [out]

Type: <b>UINT32*</b>

Actual number of geometries <i>hitTestMetrics</i> holds in its buffer memory.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

