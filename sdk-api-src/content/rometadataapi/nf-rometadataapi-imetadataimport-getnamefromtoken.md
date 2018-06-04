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

# IMetaDataImport::GetNameFromToken


## -description


Gets the UTF-8 name of the object referenced by the specified metadata token. This method is obsolete.


## -parameters




### -param tk [in]

The token representing the object to return the name for.


### -param pszUtf8NamePtr [out]

A pointer to the UTF-8 object name in the heap.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>GetNameFromToken</b> is obsolete. As an alternative, call a method to get the properties of the particular type of token required, such as <a href="https://msdn.microsoft.com/6c935c4c-a7ac-49b9-af26-25f240ef78f2">GetFieldProps</a> for a field or <a href="https://msdn.microsoft.com/973f2a8c-025d-4d27-ac99-56902b1132dd">GetMethodProps</a> for a method.






## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

