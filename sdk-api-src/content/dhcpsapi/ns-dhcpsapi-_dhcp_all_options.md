---
UID: NS:dhcpsapi._DHCP_ALL_OPTIONS
title: "_DHCP_ALL_OPTIONS"
author: windows-sdk-content
description: Defines the set of all options available on a DHCP server.
old-location: dhcp\dhcp_all_options.htm
old-project: dhcp
ms.assetid: b02e3582-c99b-4d5a-aaae-c2fefd7dfaf9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_ALL_OPTIONS, DHCP_ALL_OPTIONS, DHCP_ALL_OPTIONS structure [DHCP], LPDHCP_ALL_OPTIONS, LPDHCP_ALL_OPTIONS structure pointer [DHCP], _DHCP_ALL_OPTIONS, dhcp.dhcp_all_options, dhcpsapi/LPDHCP_ALL_OPTIONS, dhcpsapi/_DHCP_ALL_OPTIONS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
req.typenames: DHCP_ALL_OPTIONS, *LPDHCP_ALL_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_ALL_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_ALL_OPTIONS structure


## -description


The <b>DHCP_ALL_OPTIONS</b> structure defines the set of all options available on a DHCP server.


## -struct-fields




### -field Flags

Reserved. This value should be set to 0.


### -field NonVendorOptions


<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a> structure that contains the set of non-vendor options.


### -field NumVendorOptions

Specifies the number of vendor options listed in <b>VendorOptions</b>.


### -field Option

 


### -field VendorName

 


### -field ClassName

 


### -field size_is

 


### -field size_is.NumVendorOptions

 


### -field VendorOptions

 




#### - *VendorOptions

Pointer to a list of structures that contain the following fields.



#### Option


<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structure that contains specific information describing the option.



#### VendorName

Unicode string that contains the name of the vendor for the option.



#### ClassName

Unicode string that contains the name of the DHCP class for the option.

