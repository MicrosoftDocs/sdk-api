---
UID: NF:structuredquery.IRelationship.MetaData
title: IRelationship::MetaData method
author: windows-driver-content
description: Retrieves an enumeration of IMetaData objects for this relationship.
old-location: search\_search_IRelationship_MetaData.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\metadata.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IRelationship, IRelationship interface [search], MetaData method, IRelationship::MetaData, MetaData method [search], MetaData method [search], IRelationship interface, MetaData,IRelationship.MetaData, _search_IRelationship_MetaData, search._search_IRelationship_MetaData, structuredquery/IRelationship::MetaData
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
-	IRelationship.MetaData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRelationship::MetaData method


## -description



          Retrieves an enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects for this relationship.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


                The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
            


### -param pMetaData [out, retval]

Type: <b>void**</b>


                Receives a pointer to the enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects. There may be multiple pairs with the same key (or the same value).
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



