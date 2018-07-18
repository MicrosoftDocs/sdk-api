---
UID: NE:drt.drt_scope_tag
title: drt_scope_tag
author: windows-sdk-content
description: The DRT_SCOPE enumeration defines the set of IPv6 scopes in which DRT operates while using the IPv6 UDP transport created by DrtCreateIpv6UdpTransport.
old-location: p2p\drt_scope.htm
old-project: P2PSdk
ms.assetid: 0b144ec0-c2d7-4996-84a0-4ab137285a30
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DRT_GLOBAL_SCOPE, DRT_LINK_LOCAL_SCOPE, DRT_SCOPE, DRT_SCOPE enumeration [Peer Networking], DRT_SITE_LOCAL_SCOPE, drt/DRT_GLOBAL_SCOPE, drt/DRT_LINK_LOCAL_SCOPE, drt/DRT_SCOPE, drt/DRT_SITE_LOCAL_SCOPE, drt_scope_tag, p2p.drt_scope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.typenames: DRT_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_SCOPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

