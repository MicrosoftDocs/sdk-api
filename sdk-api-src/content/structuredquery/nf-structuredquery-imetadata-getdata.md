---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



