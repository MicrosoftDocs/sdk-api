---
UID: NE:netfw._INET_FIREWALL_AC_CREATION_TYPE
title: INET_FIREWALL_AC_CREATION_TYPE (netfw.h)
description: Specifies the type of app container creation events for which notifications will be delivered.
helpviewer_keywords: ["INET_FIREWALL_AC_BINARY","INET_FIREWALL_AC_CREATION_TYPE","INET_FIREWALL_AC_CREATION_TYPE enumeration [ICS/ICF]","INET_FIREWALL_AC_MAX","INET_FIREWALL_AC_NONE","INET_FIREWALL_AC_PACKAGE_ID_ONLY","ics.inet_firewall_ac_creation_type","networkisolation/INET_FIREWALL_AC_BINARY","networkisolation/INET_FIREWALL_AC_CREATION_TYPE","networkisolation/INET_FIREWALL_AC_MAX","networkisolation/INET_FIREWALL_AC_NONE","networkisolation/INET_FIREWALL_AC_PACKAGE_ID_ONLY"]
old-location: ics\inet_firewall_ac_creation_type.htm
tech.root: ics
ms.assetid: 01a1f735-889e-424e-860e-ca86f0abd126
ms.date: 12/05/2018
ms.keywords: INET_FIREWALL_AC_BINARY, INET_FIREWALL_AC_CREATION_TYPE, INET_FIREWALL_AC_CREATION_TYPE enumeration [ICS/ICF], INET_FIREWALL_AC_MAX, INET_FIREWALL_AC_NONE, INET_FIREWALL_AC_PACKAGE_ID_ONLY, ics.inet_firewall_ac_creation_type, networkisolation/INET_FIREWALL_AC_BINARY, networkisolation/INET_FIREWALL_AC_CREATION_TYPE, networkisolation/INET_FIREWALL_AC_MAX, networkisolation/INET_FIREWALL_AC_NONE, networkisolation/INET_FIREWALL_AC_PACKAGE_ID_ONLY
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
req.typenames: INET_FIREWALL_AC_CREATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INET_FIREWALL_AC_CREATION_TYPE
 - netfw/_INET_FIREWALL_AC_CREATION_TYPE
 - INET_FIREWALL_AC_CREATION_TYPE
 - netfw/INET_FIREWALL_AC_CREATION_TYPE
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
 - INET_FIREWALL_AC_CREATION_TYPE
---

# INET_FIREWALL_AC_CREATION_TYPE enumeration


## -description

The <b>INET_FIREWALL_AC_CREATION_TYPE</b> enumeration specifies the type of app container creation events for which notifications will be delivered.

## -enum-fields

### -field INET_FIREWALL_AC_NONE:0x00

This value is reserved for system use.

### -field INET_FIREWALL_AC_PACKAGE_ID_ONLY:0x01

Notifications will be delivered when an app container is created with a package identifier.

### -field INET_FIREWALL_AC_BINARY:0x02

Notifications will be delivered when an app container is created with a binary path.

### -field INET_FIREWALL_AC_MAX:0x04

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_change">INET_FIREWALL_AC_CHANGE</a>
