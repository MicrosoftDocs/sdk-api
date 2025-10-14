---
UID: NS:wnvapi._WNV_IP_ADDRESS
title: WNV_IP_ADDRESS (wnvapi.h)
description: Defines an IP address object.
helpviewer_keywords: ["*PWNV_IP_ADDRESS","PWNV_IP_ADDRESS","PWNV_IP_ADDRESS structure pointer [Windows Network Virtualization]","WNV_IP_ADDRESS","WNV_IP_ADDRESS structure [Windows Network Virtualization]","wnv.wnv_ip_address","wnvapi/PWNV_IP_ADDRESS","wnvapi/WNV_IP_ADDRESS"]
old-location: wnv\wnv_ip_address.htm
tech.root: wnv
ms.assetid: 1FD137B6-74F4-4E75-A77E-65F093938662
ms.date: 12/05/2018
ms.keywords: '*PWNV_IP_ADDRESS, PWNV_IP_ADDRESS, PWNV_IP_ADDRESS structure pointer [Windows Network Virtualization], WNV_IP_ADDRESS, WNV_IP_ADDRESS structure [Windows Network Virtualization], wnv.wnv_ip_address, wnvapi/PWNV_IP_ADDRESS, wnvapi/WNV_IP_ADDRESS'
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: WNV_IP_ADDRESS, *PWNV_IP_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_IP_ADDRESS
 - wnvapi/_WNV_IP_ADDRESS
 - PWNV_IP_ADDRESS
 - wnvapi/PWNV_IP_ADDRESS
 - WNV_IP_ADDRESS
 - wnvapi/WNV_IP_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_IP_ADDRESS
---

# WNV_IP_ADDRESS structure


## -description

Defines an IP address object.

## -struct-fields

### -field IP

An IP version 4 (IPv4) or IP version 6 (IPv6) address object.

### -field IP.v4

Type: <b>IN_ADDR</b>

An IPv4 address.

### -field IP.v6

Type: <b>IN6_ADDR</b>

An IPv6 address.

### -field IP.Addr

Type: <b>UCHAR[sizeof(IN6_ADDR)]</b>

An array of bytes that contains the IP address.

## -remarks

The <b>ADDRESS_FAMILY</b> value is always specified separately in the structures that contain this IP address object.

