---
UID: NN:dwrite.IDWriteTextAnalysisSink
title: IDWriteTextAnalysisSink (dwrite.h)
description: This interface is implemented by the text analyzer's client to receive the output of a given text analysis.
helpviewer_keywords: ["IDWriteTextAnalysisSink","IDWriteTextAnalysisSink interface [Direct Write]","IDWriteTextAnalysisSink interface [Direct Write]","described","directwrite.idwritetextanalysissink","dwrite/IDWriteTextAnalysisSink"]
old-location: directwrite\idwritetextanalysissink.htm
tech.root: DirectWrite
ms.assetid: 1fd2ca46-006c-4b01-8258-6c24f4be1641
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink, IDWriteTextAnalysisSink interface [Direct Write], IDWriteTextAnalysisSink interface [Direct Write],described, directwrite.idwritetextanalysissink, dwrite/IDWriteTextAnalysisSink
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
 - IDWriteTextAnalysisSink
 - dwrite/IDWriteTextAnalysisSink
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
 - IDWriteTextAnalysisSink
---

# IDWriteTextAnalysisSink interface


## -description

This interface is implemented by the text analyzer's client to receive the
 output of a given text analysis.

## -inheritance

The <b>IDWriteTextAnalysisSink</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextAnalysisSink</b> also has these types of members:

## -remarks

The text analyzer disregards any current
 state of the analysis sink, therefore, a Set method call on a range overwrites the previously set analysis result of the same range.

