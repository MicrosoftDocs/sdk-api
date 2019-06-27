---
UID: NF:dwrite_1.IDWriteFontFace1.HasKerningPairs
title: IDWriteFontFace1::HasKerningPairs (dwrite_1.h)
author: windows-sdk-content
description: Determines whether the font supports pair-kerning.
old-location: directwrite\idwritefontface1_haskerningpairs.htm
tech.root: DirectWrite
ms.assetid: 701B874A-BA95-43CA-8762-70BA571FDC10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HasKerningPairs, HasKerningPairs method [Direct Write], HasKerningPairs method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],HasKerningPairs method, IDWriteFontFace1.HasKerningPairs, IDWriteFontFace1::HasKerningPairs, directwrite.idwritefontface1_haskerningpairs, dwrite_1/IDWriteFontFace1::HasKerningPairs
ms.topic: method
f1_keywords: 
 - "dwrite_1/IDWriteFontFace1.HasKerningPairs"
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFontFace1.HasKerningPairs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace1::HasKerningPairs


## -description


Determines whether the font supports pair-kerning.


## -parameters






## -returns



Returns TRUE if the font supports kerning pairs, otherwise FALSE.




## -remarks



If the font doesn't support pair table kerning, you don't need to
    call <a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments">IDWriteFontFace1::GetKerningPairAdjustments</a> because it would retrieve all zeroes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments">IDWriteFontFace1::GetKerningPairAdjustments</a>
 

 

