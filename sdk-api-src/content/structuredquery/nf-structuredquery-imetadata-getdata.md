---
UID: NF:structuredquery.IMetaData.GetData
title: IMetaData::GetData
author: windows-sdk-content
description: Retrieves one key/value pair from the metadata of an IEntity, IRelationship, or ISchemaProvider object.
old-location: search\_search_IMetaData_GetData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\imetadata\getdata.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetData, GetData method [search], GetData method [search],IMetaData interface, IMetaData interface [search],GetData method, IMetaData.GetData, IMetaData::GetData, _search_IMetaData_GetData, search._search_IMetaData_GetData, structuredquery/IMetaData::GetData
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
 - IMetaData.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IMetaData::GetData


## -description


Retrieves one key/value pair from the metadata of an <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>, <a href="https://msdn.microsoft.com/137f8b7c-568e-469f-83de-468cb6e50319">IRelationship</a>, or <a href="https://msdn.microsoft.com/c6cb1da0-5072-41b2-aa64-e39c8c97b2f8">ISchemaProvider</a> object.

        


## -parameters




### -param ppszKey [out]

Type: <b>LPCWSTR*</b>

Receives the key of the metadata pair as a Unicode string. The calling application must free the returned string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.
        


### -param ppszValue [out]

Type: <b>LPWSTR*</b>

Receives the value of the metadata pair as a Unicode string. The calling application must free the returned string by calling <a href="_com_CoTaskMemFree">CoTaskMemFree</a>. 

        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



