---
UID: NF:structuredquery.ISchemaProvider.GetEntity
title: ISchemaProvider::GetEntity
author: windows-sdk-content
description: Retrieves an entity by name from the loaded schema.
old-location: search\_search_ISchemaProvider_GetEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\getentity.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetEntity, GetEntity method [search], GetEntity method [search],ISchemaProvider interface, ISchemaProvider interface [search],GetEntity method, ISchemaProvider.GetEntity, ISchemaProvider::GetEntity, _search_ISchemaProvider_GetEntity, search._search_ISchemaProvider_GetEntity, structuredquery/ISchemaProvider::GetEntity
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
 - ISchemaProvider.GetEntity
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISchemaProvider::GetEntity


## -description


Retrieves an entity by name from the loaded schema. 


## -parameters




### -param pszEntityName [in]

Type: <b>LPCWSTR</b>

The name of the entity being requested.
        


### -param pEntity [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb231373(v=VS.85).aspx">IEntity</a>**</b>

Receives the address of a pointer to the requested entity. The calling application must release the entity by calling its <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. If there is no entity with the specified name, this parameter is set to <b>NULL</b>.
        


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there is no entity with the specified name, or an error value otherwise.
        



