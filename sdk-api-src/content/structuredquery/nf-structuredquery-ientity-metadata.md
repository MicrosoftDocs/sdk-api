---
UID: NF:structuredquery.IEntity.MetaData
title: IEntity::MetaData method
author: windows-driver-content
description: Retrieves an enumeration of IMetaData objects for this entity.
old-location: search\_search_IEntity_MetaData.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\metadata.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IEntity, IEntity interface [search], MetaData method, IEntity::MetaData, MetaData method [search], MetaData method [search], IEntity interface, MetaData,IEntity.MetaData, _search_IEntity_MetaData, search._search_IEntity_MetaData, structuredquery/IEntity::MetaData
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
-	IEntity.MetaData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEntity::MetaData method


## -description



          Retrieves an enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects for this entity.
        


## -parameters




### -param riid [in]

Type: <b>REFIID</b>


                The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
            


### -param pMetaData [out, retval]

Type: <b>void**</b>


                Receives the address of a pointer to an enumeration of <a href="https://msdn.microsoft.com/2647af6d-af05-4f0d-8613-03248385abec">IMetaData</a> objects.
            


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



