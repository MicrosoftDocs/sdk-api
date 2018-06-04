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

# __MIDL___MIDL_itf_winsync_0000_0000_0008 enumeration


## -description


Indicates the type of information that is included in a change batch during filtered synchronization.




## -enum-fields




### -field FT_CURRENT_ITEMS_ONLY

The change batch includes data and metadata for items that are currently in the filter.



### -field FT_CURRENT_ITEMS_AND_VERSIONS_FOR_MOVED_OUT_ITEMS




## -remarks



A replica that does not keep ghosts for items that are not in the filter indicates this by using <b>FT_CURRENT_ITEMS_ONLY</b>.

<div class="alert"><b>Note</b>  An item that is excluded by the filter in one replica, but is still tracked in the other replica is known as a "ghost".</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/139266e9-cd22-4548-a2b6-927328e7ce82">Windows Sync Enumerations</a>
 

 

