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

# ISimilarityTraitsMapping::CreateView


## -description


Maps a view of the file mapping for a similarity traits table file.


## -parameters




### -param minimumMappedPages [in]

Minimum number of pages of the file mapping to map to the view.


### -param accessMode [in]


<a href="https://msdn.microsoft.com/570fe290-1209-4bae-a56c-f6f663e53f87">RdcMappingAccessMode</a> enumeration value that specifies the desired access to the file mapping object.


### -param mappedView [out]

Pointer to a location that will receive the returned <a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a> interface pointer. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Data accessed through read-only views will never be modified.




## -see-also




<a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a>
 

 

