---
UID: NE:networkisolation._INET_FIREWALL_AC_CHANGE_TYPE
title: INET_FIREWALL_AC_CHANGE_TYPE (networkisolation.h)
description: Specifies which type of app container change occurred.
helpviewer_keywords: ["INET_FIREWALL_AC_CHANGE_CREATE","INET_FIREWALL_AC_CHANGE_DELETE","INET_FIREWALL_AC_CHANGE_INVALID","INET_FIREWALL_AC_CHANGE_MAX","INET_FIREWALL_AC_CHANGE_TYPE","INET_FIREWALL_AC_CHANGE_TYPE enumeration [ICS/ICF]","ics.inet_firewall_ac_change_type","networkisolation/INET_FIREWALL_AC_CHANGE_CREATE","networkisolation/INET_FIREWALL_AC_CHANGE_DELETE","networkisolation/INET_FIREWALL_AC_CHANGE_INVALID","networkisolation/INET_FIREWALL_AC_CHANGE_MAX","networkisolation/INET_FIREWALL_AC_CHANGE_TYPE"]
old-location: ics\inet_firewall_ac_change_type.htm
tech.root: ics
ms.assetid: 196f7150-185f-4234-a585-1a94d6dc24d7
ms.date: 12/05/2018
ms.keywords: INET_FIREWALL_AC_CHANGE_CREATE, INET_FIREWALL_AC_CHANGE_DELETE, INET_FIREWALL_AC_CHANGE_INVALID, INET_FIREWALL_AC_CHANGE_MAX, INET_FIREWALL_AC_CHANGE_TYPE, INET_FIREWALL_AC_CHANGE_TYPE enumeration [ICS/ICF], ics.inet_firewall_ac_change_type, networkisolation/INET_FIREWALL_AC_CHANGE_CREATE, networkisolation/INET_FIREWALL_AC_CHANGE_DELETE, networkisolation/INET_FIREWALL_AC_CHANGE_INVALID, networkisolation/INET_FIREWALL_AC_CHANGE_MAX, networkisolation/INET_FIREWALL_AC_CHANGE_TYPE
req.header: networkisolation.h
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
req.typenames: INET_FIREWALL_AC_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _INET_FIREWALL_AC_CHANGE_TYPE
 - networkisolation/_INET_FIREWALL_AC_CHANGE_TYPE
 - INET_FIREWALL_AC_CHANGE_TYPE
 - networkisolation/INET_FIREWALL_AC_CHANGE_TYPE
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
 - INET_FIREWALL_AC_CHANGE_TYPE
---

# INET_FIREWALL_AC_CHANGE_TYPE enumeration


## -description

The <b>INET_FIREWALL_AC_CHANGE_TYPE</b> enumeration specifies which type of app container change occurred.

## -enum-fields

### -field INET_FIREWALL_AC_CHANGE_INVALID:0

This value is reserved for system use.

### -field INET_FIREWALL_AC_CHANGE_CREATE:1

An app container was created.

### -field INET_FIREWALL_AC_CHANGE_DELETE:2

An app container was deleted.

### -field INET_FIREWALL_AC_CHANGE_MAX:3

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_change">INET_FIREWALL_AC_CHANGE</a>
