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

# drt_scope_tag enumeration


## -description


The <b>DRT_SCOPE</b> enumeration defines the set of IPv6 scopes in which DRT operates while using the IPv6 UDP transport created by <a href="https://msdn.microsoft.com/def3120b-98b6-4e31-8166-822cea7fea69">DrtCreateIpv6UdpTransport</a>.


## -enum-fields




### -field DRT_GLOBAL_SCOPE

Uses the global scope.


### -field DRT_SITE_LOCAL_SCOPE

The <b>DRT_SITE_LOCAL_SCOPE</b> has been deprecated and should not be used.


### -field DRT_LINK_LOCAL_SCOPE

Uses the link local scope.


## -see-also




<a href="https://msdn.microsoft.com/def3120b-98b6-4e31-8166-822cea7fea69">DrtCreateIpv6UdpTransport</a>



<a href="https://msdn.microsoft.com/5bd64f10-abb8-4cba-8ebd-780a6a0c7074">DrtCreatePnrpBootstrapResolver</a>
 

 

