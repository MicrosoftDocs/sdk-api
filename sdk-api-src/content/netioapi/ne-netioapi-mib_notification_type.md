---
UID: NE:netioapi._MIB_NOTIFICATION_TYPE
title: MIB_NOTIFICATION_TYPE (netioapi.h)
description: Defines the notification type passed to a callback function when a notification occurs.
helpviewer_keywords: ["*PMIB_NOTIFICATION_TYPE","MIB_NOTIFICATION_TYPE","MIB_NOTIFICATION_TYPE enumeration [MIB]","MibAddInstance","MibDeleteInstance","MibInitialNotification","MibParameterNotification","PMIB_NOTIFICATION_TYPE","PMIB_NOTIFICATION_TYPE enumeration pointer [MIB]","_MIB_NOTIFICATION_TYPE","mib.mib_notification_type","netioapi/MIB_NOTIFICATION_TYPE","netioapi/MibAddInstance","netioapi/MibDeleteInstance","netioapi/MibInitialNotification","netioapi/MibParameterNotification","netioapi/PMIB_NOTIFICATION_TYPE"]
old-location: mib\mib_notification_type.htm
tech.root: MIB
ms.assetid: 89f6a923-d745-4f9f-82d4-c77ffc8389cd
ms.date: 12/05/2018
ms.keywords: '*PMIB_NOTIFICATION_TYPE, MIB_NOTIFICATION_TYPE, MIB_NOTIFICATION_TYPE enumeration [MIB], MibAddInstance, MibDeleteInstance, MibInitialNotification, MibParameterNotification, PMIB_NOTIFICATION_TYPE, PMIB_NOTIFICATION_TYPE enumeration pointer [MIB], _MIB_NOTIFICATION_TYPE, mib.mib_notification_type, netioapi/MIB_NOTIFICATION_TYPE, netioapi/MibAddInstance, netioapi/MibDeleteInstance, netioapi/MibInitialNotification, netioapi/MibParameterNotification, netioapi/PMIB_NOTIFICATION_TYPE'
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_NOTIFICATION_TYPE
 - netioapi/_MIB_NOTIFICATION_TYPE
 - PMIB_NOTIFICATION_TYPE
 - netioapi/PMIB_NOTIFICATION_TYPE
 - MIB_NOTIFICATION_TYPE
 - netioapi/MIB_NOTIFICATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_NOTIFICATION_TYPE
---

# MIB_NOTIFICATION_TYPE enumeration


## -description

The <b>MIB_NOTIFICATION_TYPE</b> enumeration defines the notification type passed to a callback function when a notification occurs.

## -enum-fields

### -field MibParameterNotification

A parameter was changed.

### -field MibAddInstance

A new MIB instance was added.

### -field MibDeleteInstance

An existing MIB instance was deleted.

### -field MibInitialNotification

A notification that is invoked immediately after registration for change notification completes. This initial notification does not indicate a change occurred to a MIB instance. The purpose of this initial notification type is  to provide confirmation that the callback function is properly registered.

## -remarks

The <b>MIB_NOTIFICATION_TYPE</b> enumeration is defined on Windows Vista and later. 

On Windows Vista and later, new functions are provided to register to be notified when an IPv6 or IPv4 interface changes, a IPv6 or IPv4 unicast address changes, or an IPv6 or IPv4 route changes. These registration functions require a callback function be passed that is called when a change occurs. One of the parameters passed to the callback function when a notification occurs is a parameter containing a <b>MIB_NOTIFICATION_TYPE</b> that indicates the notification type. 

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>