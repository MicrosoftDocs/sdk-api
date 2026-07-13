---
UID: NF:dwrite.IDWriteTextAnalysisSource.GetNumberSubstitution
title: IDWriteTextAnalysisSource::GetNumberSubstitution (dwrite.h)
description: Gets the number substitution from the text range affected by the text analysis.
helpviewer_keywords: ["GetNumberSubstitution","GetNumberSubstitution method [Direct Write]","GetNumberSubstitution method [Direct Write]","IDWriteTextAnalysisSource interface","IDWriteTextAnalysisSource interface [Direct Write]","GetNumberSubstitution method","IDWriteTextAnalysisSource.GetNumberSubstitution","IDWriteTextAnalysisSource::GetNumberSubstitution","directwrite.idwritetextanalysissource_getnumbersubstitution","dwrite/IDWriteTextAnalysisSource::GetNumberSubstitution"]
old-location: directwrite\idwritetextanalysissource_getnumbersubstitution.htm
tech.root: DirectWrite
ms.assetid: 23e1539c-a58e-4123-82da-2f9d94309b05
ms.date: 12/05/2018
ms.keywords: GetNumberSubstitution, GetNumberSubstitution method [Direct Write], GetNumberSubstitution method [Direct Write],IDWriteTextAnalysisSource interface, IDWriteTextAnalysisSource interface [Direct Write],GetNumberSubstitution method, IDWriteTextAnalysisSource.GetNumberSubstitution, IDWriteTextAnalysisSource::GetNumberSubstitution, directwrite.idwritetextanalysissource_getnumbersubstitution, dwrite/IDWriteTextAnalysisSource::GetNumberSubstitution
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
 - IDWriteTextAnalysisSource::GetNumberSubstitution
 - dwrite/IDWriteTextAnalysisSource::GetNumberSubstitution
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
 - IDWriteTextAnalysisSource.GetNumberSubstitution
---

# IDWriteTextAnalysisSource::GetNumberSubstitution


## -description

Gets the number substitution from the text range affected by the text analysis.

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The starting position from which to report.

### -param textLength [out]

Type: <b>UINT32*</b>

Contains  the length of the text, in characters, remaining in the text range up to the next differing number substitution.

### -param numberSubstitution [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritenumbersubstitution">IDWriteNumberSubstitution</a>**</b>

Contains an address of a pointer to an object, which was created with <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createnumbersubstitution">IDWriteFactory::CreateNumberSubstitution</a>, that holds the appropriate digits and numeric punctuation for a given locale.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any implementation should return the number substitution with an incremented reference count, and the analysis will release when finished
     with it (either before the next call or before it returns). However,
     the sink callback may hold onto it after that.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>

