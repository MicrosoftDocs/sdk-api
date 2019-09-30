---
UID: NS:dhcpsapi._DHCP_CLASS_INFO_ARRAY
title: DHCP_CLASS_INFO_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: Defines an array of elements that contain DHCP class information.
old-location: dhcp\dhcp_class_info_array.htm
tech.root: DHCP
ms.assetid: 716beba3-cba2-406c-a41f-2f08b6a7dc5a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLASS_INFO_ARRAY, DHCP_CLASS_INFO_ARRAY, DHCP_CLASS_INFO_ARRAY structure [DHCP], LPDHCP_CLASS_INFO_ARRAY, LPDHCP_CLASS_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_class_info_array, dhcpsapi/LPDHCP_CLASS_INFO_ARRAY, dhcpsapi/_DHCP_CLASS_INFO_ARRAY'
ms.topic: struct
f1_keywords:
- dhcpsapi/DHCP_CLASS_INFO_ARRAY
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
- DHCP_CLASS_INFO_ARRAY
targetos: Windows
req.typenames: DHCP_CLASS_INFO_ARRAY, *LPDHCP_CLASS_INFO_ARRAY
req.redist: 
ms.custom: 19H1
---

# DHCP_CLASS_INFO_ARRAY structure


## -description


The <b>DHCP_CLASS_INFO_ARRAY</b> structure defines an array of elements that contain DHCP class information.


## -struct-fields




### -field NumElements

Specifies the number of elements in <b>Classes</b>.


### -field Classes

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a> structures that contain DHCP class information.


### -field Classes.size_is

 


### -field Classes.size_is.NumElements

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_class_info">DHCP_CLASS_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumclasses">DhcpEnumClasses</a>
 

 

