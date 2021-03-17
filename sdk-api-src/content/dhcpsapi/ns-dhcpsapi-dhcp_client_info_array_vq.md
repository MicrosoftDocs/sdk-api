---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY_VQ
title: DHCP_CLIENT_INFO_ARRAY_VQ (dhcpsapi.h)
description: Specifies an array of DHCP_CLIENT_INFO_VQ structures.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_ARRAY_VQ","DHCP_CLIENT_INFO_ARRAY_VQ","DHCP_CLIENT_INFO_ARRAY_VQ structure [DHCP]","PDHCP_CLIENT_INFO_ARRAY_VQ","PDHCP_CLIENT_INFO_ARRAY_VQ structure pointer [DHCP]","dhcp.dhcp_client_info_array_vq","dhcpsapi/DHCP_CLIENT_INFO_ARRAY_VQ","dhcpsapi/PDHCP_CLIENT_INFO_ARRAY_VQ"]
old-location: dhcp\dhcp_client_info_array_vq.htm
tech.root: DHCP
ms.assetid: 80474274-4ef8-4e53-85b4-78cb953e9831
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_ARRAY_VQ, DHCP_CLIENT_INFO_ARRAY_VQ, DHCP_CLIENT_INFO_ARRAY_VQ structure [DHCP], PDHCP_CLIENT_INFO_ARRAY_VQ, PDHCP_CLIENT_INFO_ARRAY_VQ structure pointer [DHCP], dhcp.dhcp_client_info_array_vq, dhcpsapi/DHCP_CLIENT_INFO_ARRAY_VQ, dhcpsapi/PDHCP_CLIENT_INFO_ARRAY_VQ'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_CLIENT_INFO_ARRAY_VQ, *LPDHCP_CLIENT_INFO_ARRAY_VQ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_ARRAY_VQ
 - dhcpsapi/_DHCP_CLIENT_INFO_ARRAY_VQ
 - LPDHCP_CLIENT_INFO_ARRAY_VQ
 - dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY_VQ
 - DHCP_CLIENT_INFO_ARRAY_VQ
 - dhcpsapi/DHCP_CLIENT_INFO_ARRAY_VQ
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_CLIENT_INFO_ARRAY_VQ
---

# DHCP_CLIENT_INFO_ARRAY_VQ structure


## -description

The <b>DHCP_CLIENT_INFO_ARRAY_VQ</b> structure specifies an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a> structures.

## -struct-fields

### -field NumElements

The number of elements in the array.

### -field Clients

Pointer to the first element in the array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a> structures.

### -field Clients.size_is

### -field Clients.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a>