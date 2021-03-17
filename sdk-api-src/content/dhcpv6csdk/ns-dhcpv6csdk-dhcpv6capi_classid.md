---
UID: NS:dhcpv6csdk._DHCPV6CAPI_CLASSID
title: DHCPV6CAPI_CLASSID (dhcpv6csdk.h)
description: Defines an IPv6 client class ID.
helpviewer_keywords: ["*LPDHCPV6CAPI_CLASSID","*PDHCPV6CAPI_CLASSID","DHCPV6CAPI_CLASSID","DHCPV6CAPI_CLASSID structure [DHCP]","LPDHCPV6CAPI_CLASSID","LPDHCPV6CAPI_CLASSID structure pointer [DHCP]","PDHCPV6CAPI_CLASSID","PDHCPV6CAPI_CLASSID structure pointer [DHCP]","dhcp.dhcpv6capi_classid","dhcpv6csdk/DHCPV6CAPI_CLASSID","dhcpv6csdk/LPDHCPV6CAPI_CLASSID","dhcpv6csdk/PDHCPV6CAPI_CLASSID"]
old-location: dhcp\dhcpv6capi_classid.htm
tech.root: DHCP
ms.assetid: 90dbc386-02d9-4631-8af3-edd34537fefc
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6CAPI_CLASSID, *PDHCPV6CAPI_CLASSID, DHCPV6CAPI_CLASSID, DHCPV6CAPI_CLASSID structure [DHCP], LPDHCPV6CAPI_CLASSID, LPDHCPV6CAPI_CLASSID structure pointer [DHCP], PDHCPV6CAPI_CLASSID, PDHCPV6CAPI_CLASSID structure pointer [DHCP], dhcp.dhcpv6capi_classid, dhcpv6csdk/DHCPV6CAPI_CLASSID, dhcpv6csdk/LPDHCPV6CAPI_CLASSID, dhcpv6csdk/PDHCPV6CAPI_CLASSID'
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: DHCPV6CAPI_CLASSID, *PDHCPV6CAPI_CLASSID, *LPDHCPV6CAPI_CLASSID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6CAPI_CLASSID
 - dhcpv6csdk/_DHCPV6CAPI_CLASSID
 - PDHCPV6CAPI_CLASSID
 - dhcpv6csdk/PDHCPV6CAPI_CLASSID
 - DHCPV6CAPI_CLASSID
 - dhcpv6csdk/DHCPV6CAPI_CLASSID
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
 - DHCPV6CAPI_CLASSID
---

# DHCPV6CAPI_CLASSID structure


## -description

The <b>DHCPV6CAPI_CLASSID</b> structure defines an IPv6 client class ID.

## -struct-fields

### -field Flags

Reserved for future use.  Must be set to 0.

### -field Data.size_is

### -field Data.size_is.nBytesData

### -field Data

Class ID binary data.

### -field nBytesData

Size of <b>Data</b>, in bytes.

