---
UID: NS:dhcpsapi._DHCP_ALL_OPTION_VALUES
title: DHCP_ALL_OPTION_VALUES (dhcpsapi.h)
description: Defines the set of all option values defined on a DHCP server, organized according to class/vendor pairing.helpviewer_keywords: ["*LPDHCP_ALL_OPTION_VALUES","DHCP_ALL_OPTION_VALUES","DHCP_ALL_OPTION_VALUES structure [DHCP]","LPDHCP_ALL_OPTION_VALUES","LPDHCP_ALL_OPTION_VALUES structure pointer [DHCP]","dhcp.dhcp_all_option_values","dhcpsapi/LPDHCP_ALL_OPTION_VALUES","dhcpsapi/_DHCP_ALL_OPTION_VALUES"]
old-location: dhcp\dhcp_all_option_values.htm
tech.root: DHCP
ms.assetid: f6641ff6-c9f0-4ceb-9509-2c394f30ad93
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_ALL_OPTION_VALUES, DHCP_ALL_OPTION_VALUES, DHCP_ALL_OPTION_VALUES structure [DHCP], LPDHCP_ALL_OPTION_VALUES, LPDHCP_ALL_OPTION_VALUES structure pointer [DHCP], dhcp.dhcp_all_option_values, dhcpsapi/LPDHCP_ALL_OPTION_VALUES, dhcpsapi/_DHCP_ALL_OPTION_VALUES'
f1_keywords:
- dhcpsapi/DHCP_ALL_OPTION_VALUES
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Dhcpsapi.h
api_name:
- DHCP_ALL_OPTION_VALUES
targetos: Windows
req.typenames: DHCP_ALL_OPTION_VALUES, *LPDHCP_ALL_OPTION_VALUES
req.redist: 
ms.custom: 19H1
---

# DHCP_ALL_OPTION_VALUES structure


## -description


The <b>DHCP_ALL_OPTION_VALUES</b> structure defines the set of all option values defined on a DHCP server, organized according to class/vendor pairing.


## -struct-fields




### -field Flags

Reserved. This field should be set to 0.


### -field NumElements

Specifies the number of elements in <b>Options</b>.


### -field ClassName

 


### -field VendorName

 


### -field IsVendor

 


### -field OptionsArray

 


### -field size_is

 


### -field size_is.NumElements

 


### -field Options

 




#### - *Options

Pointer to a list of structures that contain the option values for specific class/vendor pairs. The structure is defined as follows.



#### ClassName

Unicode string that contains the name of the DHCP class for the option list.



#### VendorName

Unicode string that contains the name of the vendor for the option list.



#### IsVendor

Specifies whether or not this set of options is vendor-specific. This value is <b>TRUE</b> if it is, and <b>FALSE</b> if it is not.



#### OptionsArray


<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_value_array">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the option values for the specified vendor/class pair.

