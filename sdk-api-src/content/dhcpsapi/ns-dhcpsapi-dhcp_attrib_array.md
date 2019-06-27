---
UID: NS:dhcpsapi._DHCP_ATTRIB_ARRAY
title: DHCP_ATTRIB_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: Defines a set of DHCP server attributes.
old-location: dhcp\dhcp_attrib_array.htm
tech.root: DHCP
ms.assetid: 2a9831ae-b0ba-4cec-b7a9-6e9d9bee82c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_ATTRIB_ARRAY, *PDHCP_ATTRIB_ARRAY, DHCP_ATTRIB_ARRAY, DHCP_ATTRIB_ARRAY structure [DHCP], PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY, PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY structure pointer [DHCP], dhcp.dhcp_attrib_array, dhcpsapi/PDHCP_ATTRIB_ARRAY *LPDHCP_ATTRIB_ARRAY, dhcpsapi/_DHCP_ATTRIB_ARRAY"
ms.topic: struct
f1_keywords: 
 - "dhcpsapi/DHCP_ATTRIB_ARRAY"
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
 - DHCP_ATTRIB_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_ATTRIB_ARRAY, *PDHCP_ATTRIB_ARRAY, *LPDHCP_ATTRIB_ARRAY
req.redist: 
ms.custom: 19H1
---

# DHCP_ATTRIB_ARRAY structure


## -description


The <b>DHCP_ATTRIB_ARRAY</b> structure defines a set of DHCP server attributes.


## -struct-fields




### -field NumElements

Specifies the number of attributes listed in <b>DhcpAttribs</b>.


### -field DhcpAttribs

Pointer to a list of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_attrib">DHCP_ATTRIB</a> structures that contain the DHCP server attributes.


### -field DhcpAttribs.size_is

 


### -field DhcpAttribs.size_is.NumElements

 



