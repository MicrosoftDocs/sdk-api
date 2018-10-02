---
UID: NS:dhcpsapi._DHCP_ALL_OPTION_VALUES_PB
title: "_DHCP_ALL_OPTION_VALUES_PB"
author: windows-sdk-content
description: The DHCP_ALL_OPTION_VALUES_PB structure defines the set of all option values for a DHCP server within a scope.
old-location: dhcp\dhcp_all_option_values_pb.htm
tech.root: DHCP
ms.assetid: 5b43263a-fea1-452b-9981-a0f2cf1c8cf0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCP_ALL_OPTION_VALUES_PB, DHCP_ALL_OPTION_VALUES_PB, DHCP_ALL_OPTION_VALUES_PB structure [DHCP], LPDHCP_ALL_OPTION_VALUES_PB, LPDHCP_ALL_OPTION_VALUES_PB structure pointer [DHCP], _DHCP_ALL_OPTION_VALUES_PB, dhcp.dhcp_all_option_values_pb, dhcpsapi/DHCP_ALL_OPTION_VALUES_PB, dhcpsapi/LPDHCP_ALL_OPTION_VALUES_PB"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_ALL_OPTION_VALUES_PB
product: Windows
targetos: Windows
req.typenames: DHCP_ALL_OPTION_VALUES_PB, *LPDHCP_ALL_OPTION_VALUES_PB
req.redist: 
---

# _DHCP_ALL_OPTION_VALUES_PB structure


## -description


The <b>DHCP_ALL_OPTION_VALUES_PB</b> structure defines the set of all option values for a DHCP server within a scope.


## -struct-fields




### -field Flags

Reserved. Must be 0.


### -field NumElements

Integer that specifies the number of elements in <b>Options</b>.


### -field PolicyName

 


### -field VendorName

 


### -field IsVendor

 


### -field OptionsArray

 


### -field size_is

 


### -field size_is.NumElements

 


### -field Options

Pointer to an array of structures that contain the set of all option values for specific vendor/policy pairs. There is one element per pair.



#### PolicyName

Pointer to a null-terminated Unicode string that represents the DHCP server policy name for the option set. <b>NULL</b> if none exists.



#### VendorName

Pointer to a null-terminated Unicode string that represents the vendor name  for the option set. <b>NULL</b> if none exists.



#### IsVendor

<b>TRUE</b> if the option set is vendor-specific. Otherwise, it is <b>FALSE</b>.



#### OptionsArray

A pointer to a <a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the set of all option values for the specified vendor/policy pair.


## -see-also




<a href="https://msdn.microsoft.com/3c2fff2f-3d79-4e0d-8a31-9917088b1413">DhcpV4GetAllOptionValues</a>
 

 

