---
UID: NS:dhcpsapi._DHCP_POL_COND_ARRAY
title: DHCP_POL_COND_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_POL_COND_ARRAY structure defines an array of DHCP server policy conditions.
old-location: dhcp\dhcp_pol_cond_array.htm
tech.root: DHCP
ms.assetid: 2A084E80-92F8-43F5-89C8-22F08CE449E9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_POL_COND_ARRAY, *PDHCP_POL_COND_ARRAY, DHCP_POL_COND_ARRAY, DHCP_POL_COND_ARRAY structure [DHCP], LPDHCP_POL_COND_ARRAY, LPDHCP_POL_COND_ARRAY structure pointer [DHCP], PDHCP_POL_COND_ARRAY, PDHCP_POL_COND_ARRAY structure pointer [DHCP], dhcp.dhcp_pol_cond_array, dhcpsapi/DHCP_POL_COND_ARRAY, dhcpsapi/LPDHCP_POL_COND_ARRAY, dhcpsapi/PDHCP_POL_COND_ARRAY"
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - dhcpsapi.h
api_name:
 - DHCP_POL_COND_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_POL_COND_ARRAY, *PDHCP_POL_COND_ARRAY, *LPDHCP_POL_COND_ARRAY
req.redist: 
---

# DHCP_POL_COND_ARRAY structure


## -description


The <b>DHCP_POL_COND_ARRAY</b> structure defines an array of DHCP server policy conditions.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server policy conditions in <i>Elements</i>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/99A36029-1CBD-4A93-B25A-A0239D1C08D7">DHCP_POL_COND</a>  structures.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 



