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

# _PNRP_RESOLVE_CRITERIA enumeration


## -description


The <b>PNRP_RESOLVE_CRITERIA</b> enumeration specifies the criteria that PNRP uses to resolve searches.


## -enum-fields




### -field PNRP_RESOLVE_CRITERIA_DEFAULT

Use the PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME criteria. This is also the default behavior if <a href="https://msdn.microsoft.com/02031191-3682-45f6-a6c5-8546153bc681">PNRPINFO</a> is not specified.


### -field PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME

Match a peer name. The resolve request excludes any  peer name registered locally on this computer.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The resolve request excludes any  peer name registered locally on this computer.


### -field PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME

Match a peer name. The matching peer name can be registered locally or remotely,  but the resolve request excludes  any peer name registered by the process making the resolve request.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address. The matching peer name can be registered locally or remotely, but the resolve request excludes  any peer name registered by the process making the resolve request.


### -field PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME

Match a peer name. The matching peer name can be registered locally or remotely.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The matching peer name can be registered locally or remotely.


## -see-also




<a href="https://msdn.microsoft.com/02031191-3682-45f6-a6c5-8546153bc681">PNRPINFO</a>



<a href="https://msdn.microsoft.com/71cca892-89e7-44d1-920d-987587eeed50">PNRP_and WSALookupServiceBegin</a>
 

 

