---
UID: NF:structuredquery.ISchemaProvider.MetaData
title: ISchemaProvider::MetaData
author: windows-sdk-content
description: Retrieves an enumeration of global IMetaData objects for the loaded schema.
old-location: search\_search_ISchemaProvider_MetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\metadata.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ISchemaProvider interface [search],MetaData method, ISchemaProvider.MetaData, ISchemaProvider::MetaData, MetaData, MetaData method [search], MetaData method [search],ISchemaProvider interface, _search_ISchemaProvider_MetaData, search._search_ISchemaProvider_MetaData, structuredquery/ISchemaProvider::MetaData
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
 - ISchemaProvider.MetaData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- COM
: 
- structuredquery.h
: 
- ISchemaProvider.MetaData
: 
---

# ISchemaProvider::MetaData


## -description


Retrieves an enumeration of global <a href="https://msdn.microsoft.com/en-us/library/Bb231366(v=VS.85).aspx">IMetaData</a> objects for the loaded schema.
      


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.
        


### -param pMetaData [out, retval]

Type: <b>void**</b>

Receives a pointer to an enumeration of the <a href="https://msdn.microsoft.com/en-us/library/Bb231366(v=VS.85).aspx">IMetaData</a> objects. The calling application must release it by calling its <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



