---
UID: NF:structuredquery.IRelationship.DefaultPhrase
title: IRelationship::DefaultPhrase method
author: windows-driver-content
description: Retrieves the default phrase to use for this relationship in restatements.
old-location: search\_search_IRelationship_DefaultPhrase.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\defaultphrase.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: DefaultPhrase method [search], DefaultPhrase method [search], IRelationship interface, DefaultPhrase,IRelationship.DefaultPhrase, IRelationship, IRelationship interface [search], DefaultPhrase method, IRelationship::DefaultPhrase, _search_IRelationship_DefaultPhrase, search._search_IRelationship_DefaultPhrase, structuredquery/IRelationship::DefaultPhrase
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
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IRelationship.DefaultPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRelationship::DefaultPhrase method


## -description



        Retrieves the default phrase to use for this relationship in restatements.
      


## -parameters




### -param ppszPhrase [out, retval]

Type: <b>LPWSTR*</b>


            Receives the default phrase as a Unicode string. The calling application must free the string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



