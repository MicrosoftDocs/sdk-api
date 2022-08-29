---
UID: NS:netfw._INET_FIREWALL_AC_CHANGE
title: INET_FIREWALL_AC_CHANGE (netfw.h)
description: The INET_FIREWALL_AC_CHANGE structure contains information about a change made to an app container. (INET_FIREWALL_AC_CHANGE)
helpviewer_keywords: ["*PINET_FIREWALL_AC_CHANGE","INET_FIREWALL_AC_CHANGE","INET_FIREWALL_AC_CHANGE structure [ICS/ICF]","PINET_FIREWALL_AC_CHANGE","PINET_FIREWALL_AC_CHANGE structure pointer [ICS/ICF]","_INET_FIREWALL_AC_CHANGE","ics.inet_firewall_ac_change","networkisolation/INET_FIREWALL_AC_CHANGE","networkisolation/PINET_FIREWALL_AC_CHANGE"]
old-location: ics\inet_firewall_ac_change.htm
tech.root: ics
ms.assetid: b5f1b85d-3538-4be3-b97b-f9207cc7063b
ms.date: 08/02/2022
ms.keywords: '*PINET_FIREWALL_AC_CHANGE, INET_FIREWALL_AC_CHANGE, INET_FIREWALL_AC_CHANGE structure [ICS/ICF], PINET_FIREWALL_AC_CHANGE, PINET_FIREWALL_AC_CHANGE structure pointer [ICS/ICF], _INET_FIREWALL_AC_CHANGE, ics.inet_firewall_ac_change, networkisolation/INET_FIREWALL_AC_CHANGE, networkisolation/PINET_FIREWALL_AC_CHANGE'
req.header: netfw.h
req.include-header: Netfw.h
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
targetos: Windows
req.typenames: INET_FIREWALL_AC_CHANGE, *PINET_FIREWALL_AC_CHANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INET_FIREWALL_AC_CHANGE
 - netfw/_INET_FIREWALL_AC_CHANGE
 - PINET_FIREWALL_AC_CHANGE
 - netfw/PINET_FIREWALL_AC_CHANGE
 - INET_FIREWALL_AC_CHANGE
 - netfw/INET_FIREWALL_AC_CHANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - INET_FIREWALL_AC_CHANGE
---

# INET_FIREWALL_AC_CHANGE structure


## -description

The <a href="/windows/desktop/api/netfw/ne-netfw-inet_firewall_ac_change_type">INET_FIREWALL_AC_CHANGE</a> structure contains information about a change made to an app container.

## -struct-fields

### -field changeType

Type: <b><a href="/windows/desktop/api/netfw/ne-netfw-inet_firewall_ac_change_type">INET_FIREWALL_AC_CHANGE_TYPE</a></b>

The type of change made.

### -field createType

Type: <b><a href="/windows/desktop/api/networkisolation/ne-networkisolation-inet_firewall_ac_creation_type">INET_FIREWALL_AC_CREATION_TYPE</a></b>

The method by which the app container was created.

### -field appContainerSid

Type: <b>SID*</b>

The package identifier of the app container

### -field userSid

Type: <b>SID*</b>

The security identifier (SID) of the user to whom the app container belongs.

### -field displayName

Type: <b>LPWSTR</b>

Friendly name of the app container.

### -field capabilities

Type: <b><a href="/windows/desktop/api/networkisolation/ns-networkisolation-inet_firewall_ac_capabilities">INET_FIREWALL_AC_CAPABILITIES</a></b>

Information about the capabilities of the changed app container.

### -field binaries

Type: <b><a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_binaries">INET_FIREWALL_AC_BINARIES</a></b>

Binary paths to the applications running in the changed app container.

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_binaries">INET_FIREWALL_AC_BINARIES</a>



<a href="/windows/desktop/api/networkisolation/ns-networkisolation-inet_firewall_ac_capabilities">INET_FIREWALL_AC_CAPABILITIES</a>



<a href="/windows/desktop/api/netfw/ne-netfw-inet_firewall_ac_change_type">INET_FIREWALL_AC_CHANGE_TYPE</a>



<a href="/windows/desktop/api/networkisolation/ne-networkisolation-inet_firewall_ac_creation_type">INET_FIREWALL_AC_CREATION_TYPE</a>
