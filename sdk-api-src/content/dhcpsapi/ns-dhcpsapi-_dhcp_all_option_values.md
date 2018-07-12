---
UID: NS:dhcpsapi._DHCP_ALL_OPTION_VALUES
title: "_DHCP_ALL_OPTION_VALUES"
author: windows-sdk-content
description: Defines the set of all option values defined on a DHCP server, organized according to class/vendor pairing.
old-location: dhcp\dhcp_all_option_values.htm
old-project: dhcp
ms.assetid: f6641ff6-c9f0-4ceb-9509-2c394f30ad93
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*LPDHCP_ALL_OPTION_VALUES, DHCP_ALL_OPTION_VALUES, DHCP_ALL_OPTION_VALUES structure [DHCP], LPDHCP_ALL_OPTION_VALUES, LPDHCP_ALL_OPTION_VALUES structure pointer [DHCP], _DHCP_ALL_OPTION_VALUES, dhcp.dhcp_all_option_values, dhcpsapi/LPDHCP_ALL_OPTION_VALUES, dhcpsapi/_DHCP_ALL_OPTION_VALUES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCP_ALL_OPTION_VALUES, *LPDHCP_ALL_OPTION_VALUES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_ALL_OPTION_VALUES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_ALL_OPTION_VALUES structure


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


<a href="https://msdn.microsoft.com/c68b9543-0d7a-46ab-babd-3868c1338d67">DHCP_OPTION_VALUE_ARRAY</a> structure that contains the option values for the specified vendor/class pair.

