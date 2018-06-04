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

# peer_record_flags_tag enumeration


## -description



      The <b>PEER_RECORD_FLAGS</b> enumeration specifies a set of flags for peer record behaviors.


## -enum-fields




### -field PEER_RECORD_FLAG_AUTOREFRESH

The peer record must be automatically refreshed any time an event for the record is raised.


### -field PEER_RECORD_FLAG_DELETED

The peer record is marked for deletion but has not yet been physically removed from the local computer.

