---
UID: NN:dwrite.IDWriteTextAnalysisSource
title: IDWriteTextAnalysisSource (dwrite.h)
description: Implemented by the text analyzer's client to provide text to the analyzer.
helpviewer_keywords: ["IDWriteTextAnalysisSource","IDWriteTextAnalysisSource interface [Direct Write]","IDWriteTextAnalysisSource interface [Direct Write]","described","directwrite.idwritetextanalysissource","dwrite/IDWriteTextAnalysisSource"]
old-location: directwrite\idwritetextanalysissource.htm
tech.root: DirectWrite
ms.assetid: 7e2a523d-9191-4f99-9e73-a7955c432126
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSource, IDWriteTextAnalysisSource interface [Direct Write], IDWriteTextAnalysisSource interface [Direct Write],described, directwrite.idwritetextanalysissource, dwrite/IDWriteTextAnalysisSource
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
 - IDWriteTextAnalysisSource
 - dwrite/IDWriteTextAnalysisSource
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
 - IDWriteTextAnalysisSource
---

# IDWriteTextAnalysisSource interface


## -description

Implemented by the text analyzer's client to provide text to the analyzer. It allows the separation between the logical view of text as a continuous stream of characters identifiable by unique text positions, and the actual memory layout of potentially discrete blocks of text in the client's backing store.

## -inheritance

The <b>IDWriteTextAnalysisSource</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextAnalysisSource</b> also has these types of members:

## -remarks

If any of these callbacks returns an error, then the analysis functions will stop prematurely and return a callback error. Note that rather than return E_NOTIMPL,
 an application should stub the method and return a constant/null and S_OK.

