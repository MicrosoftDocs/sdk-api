---
UID: NE:eaphostpeertypes._ISOLATION_STATE
title: ISOLATION_STATE (eaphostpeertypes.h)
description: Defines the set of possible isolation state values of a machine.
helpviewer_keywords: ["ISOLATION_STATE","ISOLATION_STATE enumeration [EAPHost]","ISOLATION_STATE_IN_PROBATION","ISOLATION_STATE_NOT_RESTRICTED","ISOLATION_STATE_RESTRICTED_ACCESS","ISOLATION_STATE_UNKNOWN","eaphost.isolation_state","eaphostpeertypes/ISOLATION_STATE","eaphostpeertypes/ISOLATION_STATE_IN_PROBATION","eaphostpeertypes/ISOLATION_STATE_NOT_RESTRICTED","eaphostpeertypes/ISOLATION_STATE_RESTRICTED_ACCESS","eaphostpeertypes/ISOLATION_STATE_UNKNOWN"]
old-location: eaphost\isolation_state.htm
tech.root: eaphost
ms.assetid: 460e447b-87c6-41df-8e8b-055e95426ca6
ms.date: 12/05/2018
ms.keywords: ISOLATION_STATE, ISOLATION_STATE enumeration [EAPHost], ISOLATION_STATE_IN_PROBATION, ISOLATION_STATE_NOT_RESTRICTED, ISOLATION_STATE_RESTRICTED_ACCESS, ISOLATION_STATE_UNKNOWN, eaphost.isolation_state, eaphostpeertypes/ISOLATION_STATE, eaphostpeertypes/ISOLATION_STATE_IN_PROBATION, eaphostpeertypes/ISOLATION_STATE_NOT_RESTRICTED, eaphostpeertypes/ISOLATION_STATE_RESTRICTED_ACCESS, eaphostpeertypes/ISOLATION_STATE_UNKNOWN
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISOLATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ISOLATION_STATE
 - eaphostpeertypes/_ISOLATION_STATE
 - ISOLATION_STATE
 - eaphostpeertypes/ISOLATION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaphostpeertypes.h
api_name:
 - ISOLATION_STATE
---

# ISOLATION_STATE enumeration


## -description

Defines the set of possible isolation state values of a machine.  The isolation state of a machine determines its network connectivity.

## -enum-fields

### -field ISOLATION_STATE_UNKNOWN:0

The client's access to the network is unknown.

### -field ISOLATION_STATE_NOT_RESTRICTED:1

The client has unrestricted full access to the network.

### -field ISOLATION_STATE_IN_PROBATION:2

The client has probationary access to the network for a limited amount of time during which time they must fix their system.

### -field ISOLATION_STATE_RESTRICTED_ACCESS:3

The client has restricted access to the network; the client is allowed access to some servers only from which they can obtain necessary information and patches to update themselves to become healthy.

### -field v1_enum

## -remarks

Network Access Protection (NAP) uses the <b>ISOLATION_STATE</b> value to determine if a client should be granted  network access.

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



[Implementing In-Band NAP Support for EAP Methods](/windows/win32/eaphost/enabling-in-band-nap-support)



[Implementing NAP Support for EAP Methods](/windows/win32/eaphost/implementing-nap-for-eap-methods)



<a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">NAP IsolationState</a>



<a href="/windows/desktop/api/eappapis/nc-eappapis-notificationhandler">NotificationHandler</a>
