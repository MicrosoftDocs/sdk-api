---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

