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

# _WCM_CONNECTION_COST enumeration


## -description


The <b>WCM_CONNECTION_COST</b> enumerated type determines the connection cost type and flags.


## -enum-fields




### -field WCM_CONNECTION_COST_UNKNOWN

Connection cost information is not available.


### -field WCM_CONNECTION_COST_UNRESTRICTED

The connection is unlimited and has unrestricted usage constraints.


### -field WCM_CONNECTION_COST_FIXED

Usage counts toward a fixed allotment of data which the user has already paid for (or agreed to pay for).


### -field WCM_CONNECTION_COST_VARIABLE

The connection cost is on a per-byte basis.


### -field WCM_CONNECTION_COST_OVERDATALIMIT

The connection has exceeded its data limit.


### -field WCM_CONNECTION_COST_CONGESTED

The connection is throttled due to high traffic.


### -field WCM_CONNECTION_COST_ROAMING

The connection is outside of the home network.

<div class="alert"><b>Note</b>  The <b>WCM_CONNECTION_COST_ROAMING</b> value comes directly from  the connection source. Attempts to set it directly will fail.</div>
<div> </div>

### -field WCM_CONNECTION_COST_APPROACHINGDATALIMIT

The connection is approaching its data limit.

