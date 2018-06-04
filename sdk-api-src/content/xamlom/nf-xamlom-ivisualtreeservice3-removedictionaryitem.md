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

# IVisualTreeService3::RemoveDictionaryItem


## -description


	Removes an item from a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.


## -parameters




### -param dictionaryHandle [in]

The dictionary to remove the resource from.


### -param resourceKey [in]

The key of the resource to remove.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any invalid resource references will result in the value being cleared, and <a href="https://msdn.microsoft.com/F1C11F32-9524-49D6-89DD-C89E4A81720A">IVisualTreeServiceCallback2</a>  will be notified.




## -see-also




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

