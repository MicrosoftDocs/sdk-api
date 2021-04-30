---
UID: NS:dhcpsapi._DHCP_CLASS_INFO_V6
title: DHCP_CLASS_INFO_V6 (dhcpsapi.h)
description: Contains the information for a particular DHCPv6 user class or vendor class.
helpviewer_keywords: ["*LPDHCP_CLASS_INFO_V6","DHCP_CLASS_INFO_V6","DHCP_CLASS_INFO_V6 structure [DHCP]","PDHCP_CLASS_INFO_V6","PDHCP_CLASS_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_class_info_v6","dhcpsapi/DHCP_CLASS_INFO_V6","dhcpsapi/PDHCP_CLASS_INFO_V6"]
old-location: dhcp\dhcp_class_info_v6.htm
tech.root: DHCP
ms.assetid: 76d9a46b-6958-4c29-8512-e6299b28ca01
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLASS_INFO_V6, DHCP_CLASS_INFO_V6, DHCP_CLASS_INFO_V6 structure [DHCP], PDHCP_CLASS_INFO_V6, PDHCP_CLASS_INFO_V6 structure pointer [DHCP], dhcp.dhcp_class_info_v6, dhcpsapi/DHCP_CLASS_INFO_V6, dhcpsapi/PDHCP_CLASS_INFO_V6'
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
req.typenames: DHCP_CLASS_INFO_V6, *LPDHCP_CLASS_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLASS_INFO_V6
 - dhcpsapi/_DHCP_CLASS_INFO_V6
 - LPDHCP_CLASS_INFO_V6
 - dhcpsapi/LPDHCP_CLASS_INFO_V6
 - DHCP_CLASS_INFO_V6
 - dhcpsapi/DHCP_CLASS_INFO_V6
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
 - DHCP_CLASS_INFO_V6
---

# DHCP_CLASS_INFO_V6 structure


## -description

The <b>DHCP_CLASS_INFO_V6</b> structure contains the information for a particular DHCPv6 user class or vendor class.

## -struct-fields

### -field ClassName

A pointer to a null-terminated Unicode string that contains the class name.

### -field ClassComment

A pointer to a null-terminated Unicode string that contains the comment for the class.

### -field ClassDataLength

The length of data as pointed to by <b>ClassData</b>.

### -field IsVendor

If <b>TRUE</b>, this information applies to a vendor class; if <b>FALSE</b>, it applies to a user class.

### -field EnterpriseNumber

 The vendor class identifier. It is default (0x00000000) for user class.

### -field Flags

This field MUST be set to zero (0x00000000) when sending and ignored on receipt.

### -field ClassData

Pointer to a BYTE blob that contains an array of bytes of length specified by <b>ClassDataLength</b>. This contains opaque data regarding a user class or a vendor class.

### -field ClassData.size_is

### -field ClassData.size_is.ClassDataLength

