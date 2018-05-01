---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY_VQ
title: "_DHCP_CLIENT_INFO_ARRAY_VQ"
author: windows-driver-content
description: Specifies an array of DHCP_CLIENT_INFO_VQ structures.
old-location: dhcp\dhcp_client_info_array_vq.htm
old-project: DHCP
ms.assetid: 80474274-4ef8-4e53-85b4-78cb953e9831
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_ARRAY_VQ, DHCP_CLIENT_INFO_ARRAY_VQ, DHCP_CLIENT_INFO_ARRAY_VQ structure [DHCP], PDHCP_CLIENT_INFO_ARRAY_VQ, PDHCP_CLIENT_INFO_ARRAY_VQ structure pointer [DHCP], _DHCP_CLIENT_INFO_ARRAY_VQ, dhcp.dhcp_client_info_array_vq, dhcpsapi/DHCP_CLIENT_INFO_ARRAY_VQ, dhcpsapi/PDHCP_CLIENT_INFO_ARRAY_VQ"
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
req.typenames: DHCP_CLIENT_INFO_ARRAY_VQ, *LPDHCP_CLIENT_INFO_ARRAY_VQ
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_CLIENT_INFO_ARRAY_VQ
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_INFO_ARRAY_VQ structure


## -description


The <b>DHCP_CLIENT_INFO_ARRAY_VQ</b> structure specifies an array of <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structures.


## -struct-fields




### -field NumElements

The number of elements in the array.


### -field Clients

Pointer to the first element in the array of <a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/f7bd832d-b4a4-404c-8959-e9653b62d434">DHCP_CLIENT_INFO_VQ</a>
 

 

