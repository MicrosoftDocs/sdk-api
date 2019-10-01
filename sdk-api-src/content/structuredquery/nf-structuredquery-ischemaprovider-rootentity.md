---
UID: NF:structuredquery.ISchemaProvider.RootEntity
title: ISchemaProvider::RootEntity (structuredquery.h)
author: windows-sdk-content
description: Retrieves the root entity of the loaded schema.
old-location: search\_search_ISchemaProvider_RootEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\rootentity.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISchemaProvider interface [search],RootEntity method, ISchemaProvider.RootEntity, ISchemaProvider::RootEntity, RootEntity, RootEntity method [search], RootEntity method [search],ISchemaProvider interface, _search_ISchemaProvider_RootEntity, search._search_ISchemaProvider_RootEntity, structuredquery/ISchemaProvider::RootEntity
ms.topic: method
f1_keywords: 
 - "structuredquery/ISchemaProvider.RootEntity"
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
 - ISchemaProvider.RootEntity
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISchemaProvider::RootEntity


## -description


Retrieves the root entity of the loaded schema.
      


## -parameters




### -param pRootEntity [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>**</b>

Receives a pointer to the root entity. The calling application must release it by invoking its <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



