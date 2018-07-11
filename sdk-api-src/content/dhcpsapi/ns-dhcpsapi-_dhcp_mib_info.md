---
UID: NS:dhcpsapi._DHCP_MIB_INFO
title: "_DHCP_MIB_INFO"
author: windows-sdk-content
description: Defines information returned from the DHCP-specific SNMP Management Information Block (MIB) about the current DHCP service.
old-location: dhcp\dhcp_mib_info.htm
old-project: dhcp
ms.assetid: 58f3e3a3-8246-48ff-be45-20a7eed1ed0e
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*LPDHCP_MIB_INFO, DHCP_MIB_INFO, DHCP_MIB_INFO structure [DHCP], LPDHCP_MIB_INFO, LPDHCP_MIB_INFO structure pointer [DHCP], _DHCP_MIB_INFO, dhcp.dhcp_mib_info, dhcpsapi/LPDHCP_MIB_INFO, dhcpsapi/_DHCP_MIB_INFO"
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
tech.root: 
req.typenames: DHCP_MIB_INFO, *LPDHCP_MIB_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_MIB_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_MIB_INFO structure


## -description


The <b>DHCP_MIB_INFO</b> structure defines information returned from the DHCP-specific SNMP Management Information Block (MIB) about the current DHCP service.


## -struct-fields




### -field Discovers

Contains the number of DHCP discovery messages received.


### -field Offers

Contains the number of DHCP service offer messages transmitted.


### -field Requests

Contains the number of dynamic address request messages received.


### -field Acks

Contains the number of DHCP ACK messages received.


### -field Naks

Contains the number of DHCP NACK messages received.


### -field Declines

Contains the number of dynamic address service decline messages received.


### -field Releases

Contains the number of dynamic address release messages received.


### -field ServerStartTime


<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a> structure that contains the date and time the DHCP service started.


### -field Scopes

Contains the number of scopes defined on the DHCP server.


### -field ScopeInfo

Array of <a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a> structures that contain information on each subnet defined on the server. There are exactly <b>Scopes</b> elements in this array. If no subnets are defined (<b>Scopes</b> is 0), this field will be <b>NULL</b>.


### -field ScopeInfo.size_is

 


### -field ScopeInfo.size_is.Scopes

 




## -see-also




<a href="https://msdn.microsoft.com/2aca69b1-b7e5-4fda-b706-ed659d86cbd5">DATE_TIME</a>



<a href="https://msdn.microsoft.com/54f54734-3e4a-489f-a61d-85fd436d28ad">SCOPE_MIB_INFO</a>
 

 

