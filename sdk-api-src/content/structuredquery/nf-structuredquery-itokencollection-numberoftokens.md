---
UID: NF:structuredquery.ITokenCollection.NumberOfTokens
title: ITokenCollection::NumberOfTokens
author: windows-sdk-content
description: Retrieves the number of tokens in the collection.
old-location: search\_search_ITokenCollection_NumberOfTokens.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\itokencollection\numberoftokens.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ITokenCollection interface [search],NumberOfTokens method, ITokenCollection.NumberOfTokens, ITokenCollection::NumberOfTokens, NumberOfTokens, NumberOfTokens method [search], NumberOfTokens method [search],ITokenCollection interface, _search_ITokenCollection_NumberOfTokens, search._search_ITokenCollection_NumberOfTokens, structuredquery/ITokenCollection::NumberOfTokens
ms.prod: windows
ms.technology: windows-sdk
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
 - ITokenCollection.NumberOfTokens
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITokenCollection::NumberOfTokens


## -description



      Retrieves the number of tokens in the collection.


## -parameters




### -param pCount [out]

Type: <b>ULONG*</b>


          Receives the number of tokens within the collection.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



