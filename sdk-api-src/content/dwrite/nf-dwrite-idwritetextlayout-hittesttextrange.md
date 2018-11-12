---
UID: NF:dwrite.IDWriteTextLayout.HitTestTextRange
title: IDWriteTextLayout::HitTestTextRange
author: windows-sdk-content
description: The application calls this function to get a set of hit-test metrics corresponding to a range of text positions.
old-location: directwrite\IDWriteTextLayout_HitTestTextRange.htm
tech.root: DirectWrite
ms.assetid: 970ea72c-d097-42c2-9d93-774387ba7881
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: HitTestTextRange, HitTestTextRange method [Direct Write], HitTestTextRange method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],HitTestTextRange method, IDWriteTextLayout.HitTestTextRange, IDWriteTextLayout::HitTestTextRange, directwrite.IDWriteTextLayout_HitTestTextRange, dwrite/IDWriteTextLayout::HitTestTextRange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteTextLayout.HitTestTextRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::HitTestTextRange


## -description


 The application calls this function to get a set of hit-test metrics
     corresponding to a range of text positions. One of the main usages
     is to implement highlight selection of the text string. The
     function returns E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), when the buffer size of
     hitTestMetrics is too small to hold all the regions calculated by the
     function. In this situation, the function sets the output value
     *actualHitTestMetricsCount to the number of geometries calculated.
     The application is responsible for allocating a new buffer of greater
     size and calling the function again.
    
     A good value to use as an initial value for maxHitTestMetricsCount may
     be calculated from the following equation:
         maxHitTestMetricsCount = lineCount * maxBidiReorderingDepth
    
     where lineCount is obtained from the value of the output argument
     *actualLineCount (from the function <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>::GetLineLengths),
     and the maxBidiReorderingDepth value from the <a href="https://msdn.microsoft.com/4524ace3-fca6-4daf-9ecb-516771e53fc9">DWRITE_TEXT_METRICS</a>structure of the output argument *textMetrics (from the function
     <a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>::<a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">CreateTextLayout</a>).


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

Type: <b><a href="https://msdn.microsoft.com/00aaed92-7078-4823-95c5-855c063c744a">DWRITE_HIT_TEST_METRICS</a>*</b>

When this method returns, contains a pointer to a buffer of the output geometry fully enclosing the specified position range.  The buffer must be at least as large as <i>maxHitTestMetricsCount</i>.


### -param maxHitTestMetricsCount

Type: <b>UINT32</b>

Maximum number of boxes <i>hitTestMetrics</i> could hold in its buffer memory.


### -param actualHitTestMetricsCount [out]

Type: <b>UINT32*</b>

Actual number of geometries <i>hitTestMetrics</i> holds in its buffer memory.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

