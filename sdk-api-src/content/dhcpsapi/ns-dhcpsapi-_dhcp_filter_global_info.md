---
UID: NS:dhcpsapi._DHCP_FILTER_GLOBAL_INFO
title: "_DHCP_FILTER_GLOBAL_INFO"
author: windows-sdk-content
description: Contains information about the enabling and disabling of the allow and deny filter lists.
old-location: dhcp\dhcp_filter_global_info.htm
tech.root: DHCP
ms.assetid: babf9cdb-bd43-41ea-9cb4-209ff129b0f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_FILTER_GLOBAL_INFO, DHCP_FILTER_GLOBAL_INFO, DHCP_FILTER_GLOBAL_INFO structure [DHCP], PDHCP_FILTER_GLOBAL_INFO, PDHCP_FILTER_GLOBAL_INFO structure pointer [DHCP], _DHCP_FILTER_GLOBAL_INFO, dhcp.dhcp_filter_global_info, dhcpsapi/DHCP_FILTER_GLOBAL_INFO, dhcpsapi/PDHCP_FILTER_GLOBAL_INFO"
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
 - DHCP_FILTER_GLOBAL_INFO
product: Windows
targetos: Windows
req.typenames: DHCP_FILTER_GLOBAL_INFO, *LPDHCP_FILTER_GLOBAL_INFO
req.redist: 
---

# _DHCP_FILTER_GLOBAL_INFO structure


## -description


The <b>DHCP_FILTER_GLOBAL_INFO</b> structure contains information about the enabling and disabling of the allow and deny filter lists.


## -struct-fields




### -field EnforceAllowList

If <b>TRUE</b>, the allow list is enabled; if <b>FALSE</b>, it is disabled.


### -field EnforceDenyList

If <b>TRUE</b>, the deny list is enabled; if <b>FALSE</b>, it is disabled.

