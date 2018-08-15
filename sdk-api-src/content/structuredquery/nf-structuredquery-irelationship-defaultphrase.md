---
UID: NF:structuredquery.IRelationship.DefaultPhrase
title: IRelationship::DefaultPhrase
author: windows-sdk-content
description: Retrieves the default phrase to use for this relationship in restatements.
old-location: search\_search_IRelationship_DefaultPhrase.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\defaultphrase.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],IRelationship interface, IRelationship interface [search],DefaultPhrase method, IRelationship.DefaultPhrase, IRelationship::DefaultPhrase, _search_IRelationship_DefaultPhrase, search._search_IRelationship_DefaultPhrase, structuredquery/IRelationship::DefaultPhrase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: structuredquery.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IRelationship.DefaultPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRelationship::DefaultPhrase


## -description


Retrieves the default phrase to use for this relationship in restatements.
      


## -parameters




### -param ppszPhrase [out, retval]

Type: <b>LPWSTR*</b>

Receives the default phrase as a Unicode string. The calling application must free the string by calling <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



