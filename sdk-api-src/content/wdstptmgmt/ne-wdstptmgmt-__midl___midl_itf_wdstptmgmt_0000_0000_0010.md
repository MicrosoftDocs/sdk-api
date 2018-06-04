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

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0010 enumeration


## -description


Specifies the type of automatic actions a WDS transport server, running on Windows Server 2008 R2, should use to handle a client computer that is slowing the multicast transmission.   


## -enum-fields




### -field WdsTptSlowClientHandlingUnknown

Default value that indicates the automatic action used to handle slow client computers is not known.


### -field WdsTptSlowClientHandlingNone

Indicates that the server takes no action on any clients that are slowing the multicast transmission.


### -field WdsTptSlowClientHandlingAutoDisconnect

Indicates that the server detects clients that are slowing the multicast transmission below a configured threshold. Depending on a configurable setting, the server disconnects the slow clients from the multicast transmission or instructs the slow clients to fallback to an alternate mechanism for retrieving data. For example, a client disconnected from a multicast session can try using unicast instead.



### -field WdsTptSlowClientHandlingMultistream

Indicates that the server detects clients that are slowing the multicast transmission below a specified percentage of available bandwidth. The server moves the slow clients to lower-speed streams of the same multicast transmission. The server cannot move legacy clients that do not support the multistream handling option, and in this case, the server disconnects the client or instructs the client to fallback depending upon the <a href="https://msdn.microsoft.com/cce0ba98-382a-45d5-8381-06864061c529">SlowClientFallback</a> property.

