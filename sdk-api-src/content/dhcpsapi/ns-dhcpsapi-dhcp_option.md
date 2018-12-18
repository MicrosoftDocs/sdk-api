---
UID: NS:dhcpsapi._DHCP_OPTION
title: DHCP_OPTION
author: windows-sdk-content
description: The DHCP_OPTION structure defines a single DHCP option and any data elements associated with it.
old-location: dhcp\dhcp_option.htm
tech.root: DHCP
ms.assetid: 1be34eb4-a226-4f07-b763-173a4f8a0671
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_OPTION, DHCP_OPTION, DHCP_OPTION structure [DHCP], LPDHCP_OPTION, LPDHCP_OPTION structure pointer [DHCP], dhcp.dhcp_option, dhcpsapi/DHCP_OPTION, dhcpsapi/LPDHCP_OPTION"
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
 - DHCP_OPTION
product: Windows
targetos: Windows
req.typenames: DHCP_OPTION, *LPDHCP_OPTION
req.redist: 
---

# DHCP_OPTION structure


## -description


The <b>DHCP_OPTION</b> structure defines a single DHCP option and any data elements associated with it.


## -struct-fields




### -field OptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies a unique ID number (also called a "code") for this option.


### -field OptionName

Unicode string that contains the name of this option.


### -field OptionComment

Unicode string that contains a comment about this option.


### -field DefaultValue


<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a> structure that contains the data associated with this option.


### -field OptionType


<a href="https://msdn.microsoft.com/2577c0b6-aa84-4176-87b7-ffd304823d76">DHCP_OPTION_TYPE</a> enumeration value that indicates whether this option is a single unary item or an element in an array of options.


## -see-also




<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a>



<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a>



<a href="https://msdn.microsoft.com/2577c0b6-aa84-4176-87b7-ffd304823d76">DHCP_OPTION_TYPE</a>
 

 

