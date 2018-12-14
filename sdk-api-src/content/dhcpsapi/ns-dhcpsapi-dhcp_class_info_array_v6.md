---
UID: NS:dhcpsapi._DHCP_CLASS_INFO_ARRAY_V6
title: DHCP_CLASS_INFO_ARRAY_V6
author: windows-sdk-content
description: The DHCP_CLASS_INFO_ARRAY_V6 structure contains a list of information regarding a user class or a vendor class.
old-location: dhcp\dhcp_class_info_array_v6.htm
tech.root: DHCP
ms.assetid: b724ae08-4e18-4cad-9376-174acbd5b4f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_CLASS_INFO_ARRAY_V6, DHCP_CLASS_INFO_ARRAY_V6, DHCP_CLASS_INFO_ARRAY_V6 structure [DHCP], PDHCP_CLASS_INFO_ARRAY_V6, PDHCP_CLASS_INFO_ARRAY_V6 structure pointer [DHCP], dhcp.dhcp_class_info_array_v6, dhcpsapi/DHCP_CLASS_INFO_ARRAY_V6, dhcpsapi/PDHCP_CLASS_INFO_ARRAY_V6"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DHCP_CLASS_INFO_ARRAY_V6
product: Windows
targetos: Windows
req.typenames: DHCP_CLASS_INFO_ARRAY_V6, *LPDHCP_CLASS_INFO_ARRAY_V6
req.redist: 
---

# DHCP_CLASS_INFO_ARRAY_V6 structure


## -description


The <b>DHCP_CLASS_INFO_ARRAY_V6</b> structure contains a list of information regarding a user class or a vendor class.




## -struct-fields




### -field NumElements

This is of type <b>DWORD</b>, specifying the number of classes whose information is contained in the array specified by Classes.


### -field Classes

A pointer to an array of structures <a href="https://msdn.microsoft.com/76d9a46b-6958-4c29-8512-e6299b28ca01">DHCP_CLASS_INFO_V6</a> (section 2.2.1.2.70) that contains information regarding the various user classes and vendor classes.


### -field Classes.size_is

 


### -field Classes.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/76d9a46b-6958-4c29-8512-e6299b28ca01">DHCP_CLASS_INFO_V6</a>
 

 

