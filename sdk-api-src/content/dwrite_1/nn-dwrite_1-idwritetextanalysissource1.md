---
UID: NN:dwrite_1.IDWriteTextAnalysisSource1
title: IDWriteTextAnalysisSource1 (dwrite_1.h)
description: The interface you implement to provide needed information to the text analyzer, like the text and associated text properties.
helpviewer_keywords: ["IDWriteTextAnalysisSource1","IDWriteTextAnalysisSource1 interface [Direct Write]","IDWriteTextAnalysisSource1 interface [Direct Write]","described","directwrite.idwritetextanalysissource1","dwrite_1/IDWriteTextAnalysisSource1"]
old-location: directwrite\idwritetextanalysissource1.htm
tech.root: DirectWrite
ms.assetid: CFB9DB16-1F0B-409F-97BC-BB4B693AB3D6
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSource1, IDWriteTextAnalysisSource1 interface [Direct Write], IDWriteTextAnalysisSource1 interface [Direct Write],described, directwrite.idwritetextanalysissource1, dwrite_1/IDWriteTextAnalysisSource1
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextAnalysisSource1
 - dwrite_1/IDWriteTextAnalysisSource1
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
 - IDWriteTextAnalysisSource1
---

# IDWriteTextAnalysisSource1 interface


## -description

The interface you implement to provide needed information to  the text analyzer, like the text and associated text properties.


<div class="alert"><b>Note</b>   If any of these callbacks return an error, the analysis functions will  stop prematurely and return a callback error.  </div>
<div> </div>

## -inheritance

The <b>IDWriteTextAnalysisSource1</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>. <b>IDWriteTextAnalysisSource1</b> also has these types of members:

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>

