---
UID: NF:structuredquery.ISchemaLocalizerSupport.Localize
title: ISchemaLocalizerSupport::Localize (structuredquery.h)
description: Localizes keywords from an input string.
helpviewer_keywords: ["ISchemaLocalizerSupport interface [search]","Localize method","ISchemaLocalizerSupport.Localize","ISchemaLocalizerSupport::Localize","Localize","Localize method [search]","Localize method [search]","ISchemaLocalizerSupport interface","_search_ISchemaLocalizerSupport_Localize","search._search_ISchemaLocalizerSupport_Localize","structuredquery/ISchemaLocalizerSupport::Localize"]
old-location: search\_search_ISchemaLocalizerSupport_Localize.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemalocalizersupport\localize.htm
ms.date: 12/05/2018
ms.keywords: ISchemaLocalizerSupport interface [search],Localize method, ISchemaLocalizerSupport.Localize, ISchemaLocalizerSupport::Localize, Localize, Localize method [search], Localize method [search],ISchemaLocalizerSupport interface, _search_ISchemaLocalizerSupport_Localize, search._search_ISchemaLocalizerSupport_Localize, structuredquery/ISchemaLocalizerSupport::Localize
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
 - ISchemaLocalizerSupport::Localize
 - structuredquery/ISchemaLocalizerSupport::Localize
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
 - ISchemaLocalizerSupport.Localize
---

# ISchemaLocalizerSupport::Localize


## -description

Localizes keywords from an input string.

## -parameters

### -param pszGlobalString [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string to be localized. It may be in one of two forms: (1) a set of keywords separated by the vertical bar character (Unicode character code 007C) (for example "date modified|modified|modification date"), or (2) a string of the form "@some.dll,-12345". This example refers to resource ID 12345 of the some.dll binary. That resource must be a string of the previous (1) form.

### -param ppszLocalString [out, retval]

Type: <b>LPWSTR*</b>

Returns a null-terminated Unicode string that is the localized string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. If the method does not succeed, this parameter is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or S_FALSE otherwise.