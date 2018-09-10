---
UID: NS:dhcpsapi._DHCP_OPTION_VALUE
title: "_DHCP_OPTION_VALUE"
author: windows-sdk-content
description: The DHCP_OPTION_VALUE structure defines a DHCP option value (just the option data with an associated ID tag).
old-location: dhcp\dhcp_option_value.htm
tech.root: dhcp
ms.assetid: 6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_OPTION_VALUE, DHCP_OPTION_VALUE, DHCP_OPTION_VALUE structure [DHCP], LPDHCP_OPTION_VALUE, LPDHCP_OPTION_VALUE structure pointer [DHCP], _DHCP_OPTION_VALUE, dhcp.dhcp_option_value, dhcpsapi/LPDHCP_OPTION_VALUE, dhcpsapi/_DHCP_OPTION_VALUE"
ms.prod: windows
ms.technology: windows-sdk
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
 - DHCP_OPTION_VALUE
product: Windows
targetos: Windows
req.typenames: DHCP_OPTION_VALUE, *LPDHCP_OPTION_VALUE
req.redist: 
---

# _DHCP_OPTION_VALUE structure


## -description


The <b>DHCP_OPTION_VALUE</b> structure defines a DHCP  option value (just the option data with an associated ID tag).


## -struct-fields




### -field OptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies a unique ID number for the option.


### -field Value


<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a> structure that contains the data for a DHCP server option.


## -see-also




<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a>



<a href="https://msdn.microsoft.com/7dca800f-2427-44b1-bc92-f9db54de08a5">DhcpGetOptionValue</a>
 

 

