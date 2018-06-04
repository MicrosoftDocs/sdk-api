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

# _FsrmCollectionState enumeration


## -description


Defines the possible states of a collection object.


## -enum-fields




### -field FsrmCollectionState_Fetching

The collection object is fetching data.


### -field FsrmCollectionState_Committing

The collection object is committing its data.


### -field FsrmCollectionState_Complete

The collection object is complete (has stopped fetching or committing data).


### -field FsrmCollectionState_Cancelled

The collection operation (fetching or committing) was canceled.


## -see-also




<a href="https://msdn.microsoft.com/c12c55c1-baff-4810-ad2a-453abb6af5b5">IFsrmCollection::State</a>
 

 

