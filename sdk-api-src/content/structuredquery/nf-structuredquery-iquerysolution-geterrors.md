---
UID: NF:structuredquery.IQuerySolution.GetErrors
title: IQuerySolution::GetErrors
author: windows-sdk-content
description: Identifies parts of the input string that the parser did not recognize or did not use when constructing the IQuerySolution condition tree.
old-location: search\_search_IQuerySolution_GetErrors.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\geterrors.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetErrors, GetErrors method [search], GetErrors method [search],IQuerySolution interface, IQuerySolution interface [search],GetErrors method, IQuerySolution.GetErrors, IQuerySolution::GetErrors, _search_IQuerySolution_GetErrors, search._search_IQuerySolution_GetErrors, structuredquery/IQuerySolution::GetErrors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQuerySolution.GetErrors
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IQuerySolution::GetErrors


## -description


Identifies parts of the input string that the parser did not recognize or did not use when constructing the <a href="https://msdn.microsoft.com/a4987e80-7ad9-400d-8c6d-ec3b9a6bf3f1">IQuerySolution</a> condition tree.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
        


### -param ppParseErrors [out, retval]

Type: <b>void**</b>

Receives a pointer to an enumeration of zero or more <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> objects, each describing one parsing error.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 
        Each parsing error is represented by an <a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a> object in which the position information reflects token counts. The <b>IRichChunk</b> object <i>ppsz</i> string is <b>NULL</b>, and the <i>pValue</i> is a <a href="_stg_propvariant">PROPVARIANT</a> that contains a <b>lVal</b> identifying the <a href="https://msdn.microsoft.com/abc76a8c-ee72-469a-85a0-75c12ee4e5d9">STRUCTURED_QUERY_PARSE_ERROR</a> enumeration.
      

The valid values for <i>riid</i> are __uuidof(IEnumUnknown) and __uuidof(IEnumVARIANT).
      



