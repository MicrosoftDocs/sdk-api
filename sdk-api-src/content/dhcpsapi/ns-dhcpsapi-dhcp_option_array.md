---
UID: NS:dhcpsapi._DHCP_OPTION_ARRAY
title: DHCP_OPTION_ARRAY
author: windows-sdk-content
description: The DHCP_OPTION_ARRAY structure defines an array of DHCP server options.
old-location: dhcp\dhcp_option_array.htm
tech.root: DHCP
ms.assetid: 15b9bab5-8211-47c8-bc93-96c922c1aec1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_OPTION_ARRAY, DHCP_OPTION_ARRAY, DHCP_OPTION_ARRAY structure [DHCP], LPDHCP_OPTION_ARRAY, LPDHCP_OPTION_ARRAY structure pointer [DHCP], dhcp.dhcp_option_array, dhcpsapi/DHCP_OPTION_ARRAY, dhcpsapi/LPDHCP_OPTION_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - DHCP_OPTION_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_OPTION_ARRAY, *LPDHCP_OPTION_ARRAY
req.redist: 
---

# DHCP_OPTION_ARRAY structure


## -description


The <b>DHCP_OPTION_ARRAY</b> structure defines an array of DHCP server options.


## -struct-fields




### -field NumElements

Specifies the number of option elements in <b>Options</b>.


### -field Options

Pointer to a list of <a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a> structures containing DHCP server options and the associated data.


### -field Options.size_is

 


### -field Options.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/1be34eb4-a226-4f07-b763-173a4f8a0671">DHCP_OPTION</a>



<a href="https://msdn.microsoft.com/91d4d678-f0c5-4081-9302-0d08c8994692">DHCP_OPTION_SCOPE_INFO</a>
 

 

