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

# __MIDL___MIDL_itf_winsync_0000_0000_0007 enumeration


## -description


Represents the version of <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a> that a particular component is compatible with. For an overview of what is involved in building synchronization providers using  <a href="http://go.microsoft.com/fwlink/p/?linkid=134798">Microsoft Sync Framework</a>, see <a href="https://msdn.microsoft.com/acf9a557-da4f-4688-9fea-9456947c17b4">Options for Building a Synchronization Provider</a>.




## -enum-fields




### -field SYNC_SERIALIZATION_VERSION_V1

Indicates a component is compatible with Sync Framework 1.0.



### -field SYNC_SERIALIZATION_VERSION_V2

Indicates a component is compatible with Sync Framework 2.0.



### -field SYNC_SERIALIZATION_VERSION_V3




## -remarks



A component that is designed to work with a particular version of Sync Framework can indicate the version for which it is designed. This way, when Sync Framework changes in later versions, a component designed for an earlier version will continue to function as expected.





## -see-also




<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

