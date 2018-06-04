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

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0004 enumeration


## -description


Indicates what action a WDS client should take when it is disconnected from the session.


## -enum-fields




### -field WdsTptDisconnectUnknown

Default value that indicates that the disconnection type is not known.


### -field WdsTptDisconnectFallback

Indicates that the client should leave the session and fallback to an alternate mechanism for retrieving data. For example, a client disconnected from a multicast session can try using unicast instead.


### -field WdsTptDisconnectAbort

Indicates that the client should leave the session and abort all attempts to retrieve the data from this server.

