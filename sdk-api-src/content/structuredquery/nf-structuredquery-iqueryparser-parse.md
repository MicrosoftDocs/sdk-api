---
UID: NF:structuredquery.IQueryParser.Parse
title: IQueryParser::Parse (structuredquery.h)
description: Parses an input string that contains Structured Query keywords and/or contents to produce an IQuerySolution object.
helpviewer_keywords: ["IQueryParser interface [search]","Parse method","IQueryParser.Parse","IQueryParser::Parse","Parse","Parse method [search]","Parse method [search]","IQueryParser interface","_search_IQueryParser_Parse","search._search_IQueryParser_Parse","structuredquery/IQueryParser::Parse"]
old-location: search\_search_IQueryParser_Parse.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\parse.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser interface [search],Parse method, IQueryParser.Parse, IQueryParser::Parse, Parse, Parse method [search], Parse method [search],IQueryParser interface, _search_IQueryParser_Parse, search._search_IQueryParser_Parse, structuredquery/IQueryParser::Parse
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
 - IQueryParser::Parse
 - structuredquery/IQueryParser::Parse
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
 - IQueryParser.Parse
---

# IQueryParser::Parse


## -description

Parses an input string that contains Structured Query keywords and/or contents to produce an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object.

## -parameters

### -param pszInputString [in]

Type: <b>LPCWSTR</b>

A pointer to the Unicode input string to be parsed.

### -param pCustomProperties [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>*</b>

An enumeration of <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> objects, one for each custom property the application has recognized. This parameter can be <b>NULL</b>, which is equivalent to an empty enumeration.

### -param ppSolution [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a>**</b>

Receives an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object. The caller must release it by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For each <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> object, the position information identifies the character span of the custom property, the string value is the name of an actual property, and the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> is unused. Although any property could be used, these generic properties are included specifically for this purpose:
        

<ul>
<li>System.StructuredQuery.CustomProperty.Boolean</li>
<li>System.StructuredQuery.CustomProperty.DateTime</li>
<li>System.StructuredQuery.CustomProperty.Integer</li>
<li>System.StructuredQuery.CustomProperty.FloatingPoint</li>
<li>System.StructuredQuery.CustomProperty.String</li>
</ul>
An application can use them in the enumeration passed in the <i>pCustomProperties</i> parameter and look for them in the resulting condition tree.