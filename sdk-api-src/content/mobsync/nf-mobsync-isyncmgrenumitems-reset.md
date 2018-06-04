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

# ISyncMgrEnumItems::Reset


## -description


Instructs the enumerator to position itself at the beginning of the list of elements.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return S_OK if the method succeeds.




## -remarks



There is no guarantee that the same set of elements are enumerated on each pass through the list, nor are the elements necessarily enumerated in the same order. The exact behavior depends on the collection being enumerated. The operation is too memory-intensive for some collections, such as files in a directory, to maintain a specific state.



