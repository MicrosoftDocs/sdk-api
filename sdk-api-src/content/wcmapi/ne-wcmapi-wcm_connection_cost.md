---
UID: NE:wcmapi._WCM_CONNECTION_COST
title: WCM_CONNECTION_COST
author: windows-sdk-content
description: Determines the connection cost type and flags.
old-location: wcm\wcm_connection_cost.htm
tech.root: wcm
ms.assetid: 1ab36082-3394-42e3-aee3-01df5e211ba7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWCM_CONNECTION_COST, PWCM_CONNECTION_COST, PWCM_CONNECTION_COST enumeration pointer [Windows Connection Manager], WCM_CONNECTION_COST, WCM_CONNECTION_COST enumeration [Windows Connection Manager], WCM_CONNECTION_COST_APPROACHINGDATALIMIT, WCM_CONNECTION_COST_CONGESTED, WCM_CONNECTION_COST_FIXED, WCM_CONNECTION_COST_OVERDATALIMIT, WCM_CONNECTION_COST_ROAMING, WCM_CONNECTION_COST_UNKNOWN, WCM_CONNECTION_COST_UNRESTRICTED, WCM_CONNECTION_COST_VARIABLE, wcm.wcm_connection_cost, wcmapi/PWCM_CONNECTION_COST, wcmapi/WCM_CONNECTION_COST, wcmapi/WCM_CONNECTION_COST_APPROACHINGDATALIMIT, wcmapi/WCM_CONNECTION_COST_CONGESTED, wcmapi/WCM_CONNECTION_COST_FIXED, wcmapi/WCM_CONNECTION_COST_OVERDATALIMIT, wcmapi/WCM_CONNECTION_COST_ROAMING, wcmapi/WCM_CONNECTION_COST_UNKNOWN, wcmapi/WCM_CONNECTION_COST_UNRESTRICTED, wcmapi/WCM_CONNECTION_COST_VARIABLE"
ms.topic: enum
req.header: wcmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_CONNECTION_COST
product: Windows
targetos: Windows
req.typenames: WCM_CONNECTION_COST, *PWCM_CONNECTION_COST
req.redist: 
---

# WCM_CONNECTION_COST enumeration


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

