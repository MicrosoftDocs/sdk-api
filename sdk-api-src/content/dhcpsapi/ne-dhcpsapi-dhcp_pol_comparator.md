---
UID: NE:dhcpsapi.DHCP_POL_COMPARATOR
title: DHCP_POL_COMPARATOR
author: windows-sdk-content
description: The DHCP_POL_COMPARATOR enumeration defines the comparison operator for a condition when building a DHCP server policy.
old-location: dhcp\dhcp_pol_comparator.htm
old-project: DHCP
ms.assetid: 7b34e9ec-a3c6-4b85-bb36-d4f834912a64
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DHCP_POL_COMPARATOR, DHCP_POL_COMPARATOR enumeration [DHCP], DhcpCompBeginsWith, DhcpCompEqual, DhcpCompNotBeginWith, DhcpCompNotEqual, dhcp.dhcp_pol_comparator, dhcpsapi/DHCP_POL_COMPARATOR, dhcpsapi/DhcpCompBeginsWith, dhcpsapi/DhcpCompEqual, dhcpsapi/DhcpCompNotBeginWith, dhcpsapi/DhcpCompNotEqual
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DHCP_POL_COMPARATOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POL_COMPARATOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DHCP_POL_COMPARATOR enumeration


## -description


The <b>DHCP_POL_COMPARATOR</b> enumeration defines the comparison operator for a condition when building a DHCP server policy.


## -enum-fields




### -field DhcpCompEqual

The DHCP client message field specified by the criterion must exactly match the value supplied in the condition.


### -field DhcpCompNotEqual

The DHCP client message field specified by the criterion must not exactly match the value supplied in the condition.


### -field DhcpCompBeginsWith

The DHCP client message field specified by the criterion must begin with the value supplied in the condition.


### -field DhcpCompNotBeginWith

The DHCP client message field specified by the criterion must not begin with the value supplied in the condition.


### -field DhcpCompEndsWith


### -field DhcpCompNotEndWith




## -see-also




<a href="https://msdn.microsoft.com/99A36029-1CBD-4A93-B25A-A0239D1C08D7">DHCP_POL_COND</a>



<a href="https://msdn.microsoft.com/7c90625c-e6b5-475f-a9ea-0dfd27810f03">DhcpHlprAddV4PolicyCondition</a>
 

 

