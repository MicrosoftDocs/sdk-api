---
UID: NS:dhcpcsdk._DHCPCAPI_CLASSID
title: DHCPCAPI_CLASSID (dhcpcsdk.h)
description: The DHCPCAPI_CLASSID structure defines a client Class ID.
helpviewer_keywords: ["*LPDHCPCAPI_CLASSID","*LPDHCPCAPI_CLASSID structure [DHCP]","*PDHCPCAPI_CLASSID","*PDHCPCAPI_CLASSID structure [DHCP]","DHCPCAPI_CLASSID","DHCPCAPI_CLASSID structure [DHCP]","dhcp.dhcpcapi_classid","dhcpcsdk/*LPDHCPCAPI_CLASSID","dhcpcsdk/*PDHCPCAPI_CLASSID","dhcpcsdk/DHCPCAPI_CLASSID"]
old-location: dhcp\dhcpcapi_classid.htm
tech.root: DHCP
ms.assetid: ef1167cb-fcfb-4de3-8b3c-d306f69472f3
ms.date: 12/05/2018
ms.keywords: '*LPDHCPCAPI_CLASSID, *LPDHCPCAPI_CLASSID structure [DHCP], *PDHCPCAPI_CLASSID, *PDHCPCAPI_CLASSID structure [DHCP], DHCPCAPI_CLASSID, DHCPCAPI_CLASSID structure [DHCP], dhcp.dhcpcapi_classid, dhcpcsdk/*LPDHCPCAPI_CLASSID, dhcpcsdk/*PDHCPCAPI_CLASSID, dhcpcsdk/DHCPCAPI_CLASSID'
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: DHCPCAPI_CLASSID, *PDHCPCAPI_CLASSID, *LPDHCPCAPI_CLASSID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPCAPI_CLASSID
 - dhcpcsdk/_DHCPCAPI_CLASSID
 - PDHCPCAPI_CLASSID
 - dhcpcsdk/PDHCPCAPI_CLASSID
 - DHCPCAPI_CLASSID
 - dhcpcsdk/DHCPCAPI_CLASSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpcsdk.h
api_name:
 - DHCPCAPI_CLASSID
---

# DHCPCAPI_CLASSID structure


## -description

The <b>DHCPCAPI_CLASSID</b> structure defines a client Class ID.

## -struct-fields

### -field Flags

Reserved. Must be set to zero.

### -field Data.size_is

### -field Data.size_is.nBytesData

### -field Data

Class ID binary data.

### -field nBytesData

Size of <b>Data</b>, in bytes.

