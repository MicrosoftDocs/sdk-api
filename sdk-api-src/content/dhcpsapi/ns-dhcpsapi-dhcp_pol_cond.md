---
UID: NS:dhcpsapi._DHCP_POL_COND
title: DHCP_POL_COND (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_POL_COND structure defines the DHCP server policy condition.
old-location: dhcp\dhcp_pol_cond.htm
tech.root: DHCP
ms.assetid: 99A36029-1CBD-4A93-B25A-A0239D1C08D7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_POL_COND, *PDHCP_POL_COND, DHCP_POL_COND, DHCP_POL_COND structure [DHCP], LPDHCP_POL_COND, LPDHCP_POL_COND structure pointer [DHCP], PDHCP_POL_COND, PDHCP_POL_COND structure pointer [DHCP], dhcp.dhcp_pol_cond, dhcpsapi/DHCP_POL_COND, dhcpsapi/LPDHCP_POL_COND, dhcpsapi/PDHCP_POL_COND"
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
 - DHCP_POL_COND
product: Windows
targetos: Windows
req.typenames: DHCP_POL_COND, *PDHCP_POL_COND, *LPDHCP_POL_COND
req.redist: 
ms.custom: 19H1
---

# DHCP_POL_COND structure


## -description


The <b>DHCP_POL_COND</b> structure defines the DHCP server policy condition.


## -struct-fields




### -field ParentExpr

Integer that specifies the expression index that corresponds to this constituent condition.


### -field Type


<a href="https://msdn.microsoft.com/02a84c55-402c-40fe-8dad-6ed3f58052a1">DHCP_POL_ATTR_TYPE</a> enumeration that specifies the attribute type for this condition.


### -field OptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the unique option identifier for criteria based on DHCP options or sub-options.


### -field SubOptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies the unique sub-option identifier.


### -field VendorName

A pointer to a null-terminated Unicode string that represents the vendor name.


### -field Operator


<a href="https://msdn.microsoft.com/7b34e9ec-a3c6-4b85-bb36-d4f834912a64">DHCP_POL_COMPARATOR</a> enumeration that specifies the comparison operator for the condition.


### -field Value

Pointer to an array of bytes that contains the value to be used for the comparison.


### -field Value.size_is

 


### -field Value.size_is.ValueLength

 


### -field ValueLength

Integer that specifies the length of <b>Value</b>.


## -see-also




<a href="https://msdn.microsoft.com/2A084E80-92F8-43F5-89C8-22F08CE449E9">DHCP_POL_COND_ARRAY</a>
 

 

