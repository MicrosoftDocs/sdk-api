---
UID: NF:structuredquery.ISchemaProvider.RootEntity
title: ISchemaProvider::RootEntity
author: windows-sdk-content
description: Retrieves the root entity of the loaded schema.
old-location: search\_search_ISchemaProvider_RootEntity.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\rootentity.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISchemaProvider interface [search],RootEntity method, ISchemaProvider.RootEntity, ISchemaProvider::RootEntity, RootEntity, RootEntity method [search], RootEntity method [search],ISchemaProvider interface, _search_ISchemaProvider_RootEntity, search._search_ISchemaProvider_RootEntity, structuredquery/ISchemaProvider::RootEntity
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
 - ISchemaProvider.RootEntity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISchemaProvider::RootEntity


## -description


Retrieves the root entity of the loaded schema.
      


## -parameters




### -param pRootEntity [out, retval]

Type: <b><a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>**</b>

Receives a pointer to the root entity. The calling application must release it by invoking its <a href="_com_IUnknown_Release">IUnknown::Release</a> method.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



