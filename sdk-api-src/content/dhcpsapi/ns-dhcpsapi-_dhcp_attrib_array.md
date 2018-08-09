---
UID: NS:dhcpsapi._DHCP_ATTRIB_ARRAY
title: "_DHCP_ATTRIB_ARRAY"
author: windows-sdk-content
description: Defines a set of DHCP server attributes.
old-location: dhcp\dhcp_attrib_array.htm
old-project: dhcp
ms.assetid: 2a9831ae-b0ba-4cec-b7a9-6e9d9bee82c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_ATTRIB_ARRAY, *PDHCP_ATTRIB_ARRAY, DHCP_ATTRIB_ARRAY, DHCP_ATTRIB_ARRAY structure [DHCP], PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY, PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY structure pointer [DHCP], _DHCP_ATTRIB_ARRAY, dhcp.dhcp_attrib_array, dhcpsapi/PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY, dhcpsapi/_DHCP_ATTRIB_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_ATTRIB_ARRAY, *PDHCP_ATTRIB_ARRAY, *LPDHCP_ATTRIB_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_ATTRIB_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_ATTRIB_ARRAY structure


## -description


The <b>DHCP_ATTRIB_ARRAY</b> structure defines a set of DHCP server attributes.


## -struct-fields




### -field NumElements

Specifies the number of attributes listed in <b>DhcpAttribs</b>.


### -field DhcpAttribs

Pointer to a list of <a href="https://msdn.microsoft.com/26822137-8633-4e18-a69f-eeebf9e78f9a">DHCP_ATTRIB</a> structures that contain the DHCP server attributes.


### -field DhcpAttribs.size_is

 


### -field DhcpAttribs.size_is.NumElements

 



