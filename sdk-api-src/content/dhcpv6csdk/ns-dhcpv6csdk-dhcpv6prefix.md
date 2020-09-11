---
UID: NS:dhcpv6csdk._DHCPV6Prefix
title: DHCPV6Prefix (dhcpv6csdk.h)
description: The DHCPV6Prefix contains an IPv6 prefix.
helpviewer_keywords: ["*LPDHCPV6Prefix","*PDHCPV6Prefix","DHCPV6Prefix","DHCPV6Prefix structure [DHCP]","LPDHCPV6Prefix","LPDHCPV6Prefix structure pointer [DHCP]","PDHCPV6Prefix","PDHCPV6Prefix structure pointer [DHCP]","dhcp.dhcpv6prefix","dhcpv6csdk/DHCPV6Prefix","dhcpv6csdk/LPDHCPV6Prefix","dhcpv6csdk/PDHCPV6Prefix"]
old-location: dhcp\dhcpv6prefix.htm
tech.root: DHCP
ms.assetid: e04e3275-e4be-44bc-bd63-c45500971af7
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6Prefix, *PDHCPV6Prefix, DHCPV6Prefix, DHCPV6Prefix structure [DHCP], LPDHCPV6Prefix, LPDHCPV6Prefix structure pointer [DHCP], PDHCPV6Prefix, PDHCPV6Prefix structure pointer [DHCP], dhcp.dhcpv6prefix, dhcpv6csdk/DHCPV6Prefix, dhcpv6csdk/LPDHCPV6Prefix, dhcpv6csdk/PDHCPV6Prefix'
req.header: dhcpv6csdk.h
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
req.typenames: DHCPV6Prefix, *PDHCPV6Prefix, *LPDHCPV6Prefix
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6Prefix
 - dhcpv6csdk/_DHCPV6Prefix
 - PDHCPV6Prefix
 - dhcpv6csdk/PDHCPV6Prefix
 - DHCPV6Prefix
 - dhcpv6csdk/DHCPV6Prefix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpv6csdk.h
api_name:
 - DHCPV6Prefix
---

# DHCPV6Prefix structure


## -description

The <b>DHCPV6Prefix</b> contains an IPv6 prefix.

## -struct-fields

### -field prefix

128 bit prefix.

### -field prefixLength

Length of the prefix.

### -field preferredLifeTime

Preferred lifetime of the prefix, in seconds.

### -field validLifeTime

The valid lifetime of the prefix in seconds.

### -field status

The status code returned.

