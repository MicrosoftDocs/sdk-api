---
UID: NF:dwrite.IDWriteTextAnalysisSink.SetNumberSubstitution
title: IDWriteTextAnalysisSink::SetNumberSubstitution (dwrite.h)
description: Sets the number substitution on the text range affected by the text analysis.
helpviewer_keywords: ["IDWriteTextAnalysisSink interface [Direct Write]","SetNumberSubstitution method","IDWriteTextAnalysisSink.SetNumberSubstitution","IDWriteTextAnalysisSink::SetNumberSubstitution","SetNumberSubstitution","SetNumberSubstitution method [Direct Write]","SetNumberSubstitution method [Direct Write]","IDWriteTextAnalysisSink interface","directwrite.idwritetextanalysissink_setnumbersubstitution","dwrite/IDWriteTextAnalysisSink::SetNumberSubstitution"]
old-location: directwrite\idwritetextanalysissink_setnumbersubstitution.htm
tech.root: DirectWrite
ms.assetid: 09b00b49-702e-4cef-bf1c-397c5d572513
ms.date: 12/05/2018
ms.keywords: IDWriteTextAnalysisSink interface [Direct Write],SetNumberSubstitution method, IDWriteTextAnalysisSink.SetNumberSubstitution, IDWriteTextAnalysisSink::SetNumberSubstitution, SetNumberSubstitution, SetNumberSubstitution method [Direct Write], SetNumberSubstitution method [Direct Write],IDWriteTextAnalysisSink interface, directwrite.idwritetextanalysissink_setnumbersubstitution, dwrite/IDWriteTextAnalysisSink::SetNumberSubstitution
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
 - IDWriteTextAnalysisSink::SetNumberSubstitution
 - dwrite/IDWriteTextAnalysisSink::SetNumberSubstitution
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
 - IDWriteTextAnalysisSink.SetNumberSubstitution
---

# IDWriteTextAnalysisSink::SetNumberSubstitution


## -description

Sets the number substitution on the text range affected by the text analysis.

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The starting position from which to report.

### -param textLength

Type: <b>UINT32</b>

The number of UTF16 units of the reported range.

### -param numberSubstitution

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritenumbersubstitution">IDWriteNumberSubstitution</a>*</b>

An object that holds the appropriate digits and numeric punctuation for a given locale. Use <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createnumbersubstitution">IDWriteFactory::CreateNumberSubstitution</a> to create this object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink">IDWriteTextAnalysisSink</a>

