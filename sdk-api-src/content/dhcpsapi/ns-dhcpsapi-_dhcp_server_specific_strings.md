---
UID: NS:dhcpsapi._DHCP_SERVER_SPECIFIC_STRINGS
title: "_DHCP_SERVER_SPECIFIC_STRINGS"
author: windows-sdk-content
description: Contains the default string values for user and vendor class names.
old-location: dhcp\dhcp_server_specific_strings.htm
tech.root: DHCP
ms.assetid: 5fc52d5c-22b0-454b-bc07-8f9c4ca163e3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDHCP_SERVER_SPECIFIC_STRINGS, DHCP_SERVER_SPECIFIC_STRINGS, DHCP_SERVER_SPECIFIC_STRINGS structure [DHCP], PDHCP_SERVER_SPECIFIC_STRINGS, PDHCP_SERVER_SPECIFIC_STRINGS structure pointer [DHCP], _DHCP_SERVER_SPECIFIC_STRINGS, dhcp.dhcp_server_specific_strings, dhcpsapi/DHCP_SERVER_SPECIFIC_STRINGS, dhcpsapi/PDHCP_SERVER_SPECIFIC_STRINGS"
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
 - DHCP_SERVER_SPECIFIC_STRINGS
product: Windows
targetos: Windows
req.typenames: DHCP_SERVER_SPECIFIC_STRINGS, *LPDHCP_SERVER_SPECIFIC_STRINGS
req.redist: 
---

# _DHCP_SERVER_SPECIFIC_STRINGS structure


## -description


The <b>DHCP_SERVER_SPECIFIC_STRINGS</b> structure contains the default string values for user and vendor class names.


## -struct-fields




### -field DefaultVendorClassName

Pointer to a Unicode string that specifies the default vendor class name for the DHCP server.


### -field DefaultUserClassName

Pointer to a Unicode string that specifies the default user class name for the DHCP server.


## -see-also




<a href="https://msdn.microsoft.com/dc283fa3-6077-4010-8c71-9dc91ed2dadf">DhcpGetServerSpecificStrings</a>
 

 

