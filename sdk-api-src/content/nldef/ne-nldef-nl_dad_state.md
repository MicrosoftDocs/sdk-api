---
UID: NE:nldef.NL_DAD_STATE
title: NL_DAD_STATE
author: windows-driver-content
description: The NL_DAD_STATE enumeration type defines the duplicate address detection (DAD) state.
old-location: netvista\nl_dad_state.htm
old-project: netvista
ms.assetid: 38d88074-efac-475c-b6f6-1c65f21ed4be
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IpDadStateDeprecated, IpDadStateDuplicate, IpDadStateInvalid, IpDadStatePreferred, IpDadStateTentative, NL_DAD_STATE, NL_DAD_STATE enumeration [Network Drivers Starting with Windows Vista], NldsDeprecated, NldsDuplicate, NldsInvalid, NldsPreferred, NldsTentative, iphelper_c0c9838a-2b5e-4283-8fdd-c3605433c6f8.xml, netvista.nl_dad_state, nldef/IpDadStateDeprecated, nldef/IpDadStateDuplicate, nldef/IpDadStateInvalid, nldef/IpDadStatePreferred, nldef/IpDadStateTentative, nldef/NL_DAD_STATE, nldef/NldsDeprecated, nldef/NldsDuplicate, nldef/NldsInvalid, nldef/NldsPreferred, nldef/NldsTentative
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: nldef.h
req.include-header: Netioapi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: NL_DAD_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nldef.h
api_name:
-	NL_DAD_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NL_DAD_STATE enumeration


## -description


The NL_DAD_STATE enumeration type defines the duplicate address detection (DAD) state.


## -enum-fields




### -field NldsInvalid

Reserved for system use. Do not use this value in your driver.


### -field NldsTentative

Reserved for system use. Do not use this value in your driver.


### -field NldsDuplicate

Reserved for system use. Do not use this value in your driver.


### -field NldsDeprecated

Reserved for system use. Do not use this value in your driver.


### -field NldsPreferred

Reserved for system use. Do not use this value in your driver.


### -field IpDadStateInvalid

The DAD state is invalid.


### -field IpDadStateTentative

The DAD state is tentative.


### -field IpDadStateDuplicate

A duplicate IP address has been detected.


### -field IpDadStateDeprecated

The IP address has been deprecated.


### -field IpDadStatePreferred

The IP address is the preferred address.


## -remarks



The DAD state applies to both IPv4 and IPv6 addresses.



