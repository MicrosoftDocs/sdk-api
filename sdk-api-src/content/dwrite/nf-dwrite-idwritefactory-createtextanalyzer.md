---
UID: NF:dwrite.IDWriteFactory.CreateTextAnalyzer
title: IDWriteFactory::CreateTextAnalyzer (dwrite.h)
description: Returns an interface for performing text analysis.
helpviewer_keywords: ["CreateTextAnalyzer","CreateTextAnalyzer method [Direct Write]","CreateTextAnalyzer method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateTextAnalyzer method","IDWriteFactory.CreateTextAnalyzer","IDWriteFactory::CreateTextAnalyzer","directwrite.IDWriteFactory_CreateTextAnalyzer","dwrite/IDWriteFactory::CreateTextAnalyzer"]
old-location: directwrite\IDWriteFactory_CreateTextAnalyzer.htm
tech.root: DirectWrite
ms.assetid: 1f786de4-9498-49ef-b884-7e5f69cefe4a
ms.date: 12/05/2018
ms.keywords: CreateTextAnalyzer, CreateTextAnalyzer method [Direct Write], CreateTextAnalyzer method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextAnalyzer method, IDWriteFactory.CreateTextAnalyzer, IDWriteFactory::CreateTextAnalyzer, directwrite.IDWriteFactory_CreateTextAnalyzer, dwrite/IDWriteFactory::CreateTextAnalyzer
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
 - IDWriteFactory::CreateTextAnalyzer
 - dwrite/IDWriteFactory::CreateTextAnalyzer
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
 - IDWriteFactory.CreateTextAnalyzer
---

# IDWriteFactory::CreateTextAnalyzer


## -description

 Returns an interface for performing text analysis.

## -parameters

### -param textAnalyzer [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer">IDWriteTextAnalyzer</a>**</b>

When this method returns, contains an address of  a pointer to the newly created text analyzer object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

