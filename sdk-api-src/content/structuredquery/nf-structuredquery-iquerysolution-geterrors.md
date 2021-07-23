---
UID: NF:structuredquery.IQuerySolution.GetErrors
title: IQuerySolution::GetErrors (structuredquery.h)
description: Identifies parts of the input string that the parser did not recognize or did not use when constructing the IQuerySolution condition tree.
helpviewer_keywords: ["GetErrors","GetErrors method [search]","GetErrors method [search]","IQuerySolution interface","IQuerySolution interface [search]","GetErrors method","IQuerySolution.GetErrors","IQuerySolution::GetErrors","_search_IQuerySolution_GetErrors","search._search_IQuerySolution_GetErrors","structuredquery/IQuerySolution::GetErrors"]
old-location: search\_search_IQuerySolution_GetErrors.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\geterrors.htm
ms.date: 12/05/2018
ms.keywords: GetErrors, GetErrors method [search], GetErrors method [search],IQuerySolution interface, IQuerySolution interface [search],GetErrors method, IQuerySolution.GetErrors, IQuerySolution::GetErrors, _search_IQuerySolution_GetErrors, search._search_IQuerySolution_GetErrors, structuredquery/IQuerySolution::GetErrors
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IQuerySolution::GetErrors
 - structuredquery/IQuerySolution::GetErrors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQuerySolution.GetErrors
---

# IQuerySolution::GetErrors


## -description

Identifies parts of the input string that the parser did not recognize or did not use when constructing the <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> condition tree.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.

### -param ppParseErrors [out, retval]

Type: <b>void**</b>

Receives a pointer to an enumeration of zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> objects, each describing one parsing error.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 
        Each parsing error is represented by an <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_parse_error">IRichChunk</a> object in which the position information reflects token counts. The <b>IRichChunk</b> object <i>ppsz</i> string is <b>NULL</b>, and the <i>pValue</i> is a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> that contains a <b>lVal</b> identifying the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_parse_error">STRUCTURED_QUERY_PARSE_ERROR</a> enumeration.
      

The valid values for <i>riid</i> are __uuidof(IEnumUnknown) and __uuidof(IEnumVARIANT).