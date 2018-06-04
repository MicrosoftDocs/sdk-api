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

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0003 enumeration


## -description


Determines the type of multicast sessions used for transmitting objects covered by this namespace.


## -enum-fields




### -field WdsTptNamespaceTypeUnknown

Default value that indicates that the namespace type is not yet known. This could also be the case if a new namespace type was introduced in later server versions and this version of WdsTptMgmt has not been updated to fully recognize and classify it.


### -field WdsTptNamespaceTypeAutoCast

Indicates that multicast sessions are to be created automatically by the server based on incoming requests from clients. The server independently decides when to start or end these sessions to optimize performance and reduce network congestion.


### -field WdsTptNamespaceTypeScheduledCastManualStart

Indicates that multicast sessions for this namespace are to be scheduled such that they start only when the administrator manually launches them.


### -field WdsTptNamespaceTypeScheduledCastAutoStart

Indicates that multicast sessions for this namespace are to be automatically started by the system based on criteria the administrator sets, such as a scheduled start time or minimum number of clients.

