---
UID: NF:structuredquery.ISchemaProvider.Entities
title: ISchemaProvider::Entities
author: windows-sdk-content
description: Retrieves an enumeration of IEntity objects with one entry for each entity in the loaded schema.
old-location: search\_search_ISchemaProvider_Entities.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\entities.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: Entities, Entities method [search], Entities method [search],ISchemaProvider interface, ISchemaProvider interface [search],Entities method, ISchemaProvider.Entities, ISchemaProvider::Entities, _search_ISchemaProvider_Entities, search._search_ISchemaProvider_Entities, structuredquery/ISchemaProvider::Entities
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
 - ISchemaProvider.Entities
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISchemaProvider::Entities


## -description


Retrieves an enumeration of <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> objects with one entry for each entity in the loaded schema.
      


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
        


### -param pEntities [out, retval]

Type: <b>void**</b>

Receives a pointer to an enumeration of entities. The calling application must release it by calling its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



