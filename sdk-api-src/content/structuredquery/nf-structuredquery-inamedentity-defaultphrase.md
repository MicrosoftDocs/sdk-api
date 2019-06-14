---
UID: NF:structuredquery.INamedEntity.DefaultPhrase
title: INamedEntity::DefaultPhrase (structuredquery.h)
author: windows-sdk-content
description: Retrieves a default phrase to use for this named entity in restatements.
old-location: search\_search_INamedEntity_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentity\defaultphrase.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],INamedEntity interface, INamedEntity interface [search],DefaultPhrase method, INamedEntity.DefaultPhrase, INamedEntity::DefaultPhrase, _search_INamedEntity_DefaultPhrase, search._search_INamedEntity_DefaultPhrase, structuredquery/INamedEntity::DefaultPhrase
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
 - INamedEntity.DefaultPhrase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INamedEntity::DefaultPhrase


## -description


Retrieves a default phrase to use for this named entity in restatements.


## -parameters




### -param ppszPhrase [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the default phrase as a Unicode string. The calling application must free the returned string by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



