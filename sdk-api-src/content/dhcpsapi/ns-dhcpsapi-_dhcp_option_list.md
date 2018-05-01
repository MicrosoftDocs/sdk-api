---
UID: NS:dhcpsapi._DHCP_OPTION_LIST
title: "_DHCP_OPTION_LIST"
author: windows-driver-content
description: Defines a list of DHCP option values (just the option data with associated ID tags).
old-location: dhcp\dhcp_option_list.htm
old-project: DHCP
ms.assetid: ffe9ed82-1aec-4e09-8258-399099c87b5a
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_OPTION_LIST, DHCP_OPTION_LIST, DHCP_OPTION_LIST structure [DHCP], LPDHCP_OPTION_LIST, LPDHCP_OPTION_LIST structure pointer [DHCP], _DHCP_OPTION_LIST, dhcp.dhcp_option_list, dhcpsapi/LPDHCP_OPTION_LIST, dhcpsapi/_DHCP_OPTION_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DHCP_OPTION_LIST, *LPDHCP_OPTION_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_OPTION_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_OPTION_LIST structure


## -description


The <b>DHCP_OPTION_LIST</b> structure defines a list of DHCP option values (just the option data  with associated ID tags).


## -struct-fields




### -field NumOptions

Specifies the number of option values  listed in <b>Options</b>.


### -field Options

Pointer to a list of <a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a> structures


## -see-also




<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a>



<a href="https://msdn.microsoft.com/60f4db5f-0359-4738-980e-2a56adbf551e">DhcpGetClientOptions</a>
 

 

