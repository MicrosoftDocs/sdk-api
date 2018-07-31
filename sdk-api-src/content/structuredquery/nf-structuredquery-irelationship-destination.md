---
UID: NF:structuredquery.IRelationship.Destination
title: IRelationship::Destination
author: windows-sdk-content
description: Retrieves the destination IEntity object of the relationship. The destination of a relationshipo corresponds to the type of a property.
old-location: search\_search_IRelationship_Destination.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\destination.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Destination, Destination method [search], Destination method [search],IRelationship interface, IRelationship interface [search],Destination method, IRelationship.Destination, IRelationship::Destination, _search_IRelationship_Destination, search._search_IRelationship_Destination, structuredquery/IRelationship::Destination
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
 - IRelationship.Destination
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRelationship::Destination


## -description


Retrieves the destination <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> object of the relationship. The destination of a relationshipo corresponds to the type of a property.
      


## -parameters




### -param pDestinationEntity [out, retval]

Type: <b><a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>**</b>

Receives the address of a pointer to an <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> object, or <b>NULL</b> if the relationship is not real. For more information, see <a href="https://msdn.microsoft.com/4a209437-a382-4a28-9e1c-9eea51669791">IRelationship::IsReal</a>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



