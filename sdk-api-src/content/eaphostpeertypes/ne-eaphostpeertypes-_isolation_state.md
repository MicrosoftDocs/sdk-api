---
UID: NE:eaphostpeertypes._ISOLATION_STATE
title: "_ISOLATION_STATE"
author: windows-sdk-content
description: Defines the set of possible isolation state values of a machine.
old-location: eaphost\isolation_state.htm
old-project: eaphost
ms.assetid: 460e447b-87c6-41df-8e8b-055e95426ca6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISOLATION_STATE, ISOLATION_STATE enumeration [EAPHost], ISOLATION_STATE_IN_PROBATION, ISOLATION_STATE_NOT_RESTRICTED, ISOLATION_STATE_RESTRICTED_ACCESS, ISOLATION_STATE_UNKNOWN, _ISOLATION_STATE, eaphost.isolation_state, eaphostpeertypes/ISOLATION_STATE, eaphostpeertypes/ISOLATION_STATE_IN_PROBATION, eaphostpeertypes/ISOLATION_STATE_NOT_RESTRICTED, eaphostpeertypes/ISOLATION_STATE_RESTRICTED_ACCESS, eaphostpeertypes/ISOLATION_STATE_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: eaphostpeertypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ISOLATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaphostpeertypes.h
api_name:
 - ISOLATION_STATE
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _ISOLATION_STATE enumeration


## -description


Defines the set of possible isolation state values of a machine.  The isolation state of a machine determines its network connectivity.


## -enum-fields




### -field ISOLATION_STATE_UNKNOWN

The client's access to the network is unknown.


### -field ISOLATION_STATE_NOT_RESTRICTED

The client has unrestricted full access to the network.


### -field ISOLATION_STATE_IN_PROBATION

The client has probationary access to the network for a limited amount of time during which time they must fix their system.


### -field ISOLATION_STATE_RESTRICTED_ACCESS

The client has restricted access to the network; the client is allowed access to some servers only from which they can obtain necessary information and patches to update themselves to become healthy. 


### -field v1_enum




## -remarks



Network Access Protection (NAP) uses the <b>ISOLATION_STATE</b> value to determine if a client should be granted  network access.




## -see-also




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/298c89d9-7a6a-4280-9af9-77c7c00cab92">Implementing In-Band NAP Support for EAP Methods</a>



<a href="https://msdn.microsoft.com/c25e4f03-759a-47a7-8b35-bbe669501c5c">Implementing NAP Support for EAP Methods</a>



<a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">NAP IsolationState</a>



<a href="https://msdn.microsoft.com/7fa12cb4-694a-4db6-9743-5a2cbb995721">NotificationHandler</a>
 

 

