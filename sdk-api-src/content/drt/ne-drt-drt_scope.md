---
UID: NE:drt.drt_scope_tag
title: DRT_SCOPE (drt.h)

description: The DRT_SCOPE enumeration defines the set of IPv6 scopes in which DRT operates while using the IPv6 UDP transport created by DrtCreateIpv6UdpTransport.
old-location: p2p\drt_scope.htm
tech.root: P2PSdk
ms.assetid: 0b144ec0-c2d7-4996-84a0-4ab137285a30

ms.date: 12/05/2018
ms.keywords: DRT_GLOBAL_SCOPE, DRT_LINK_LOCAL_SCOPE, DRT_SCOPE, DRT_SCOPE enumeration [Peer Networking], DRT_SITE_LOCAL_SCOPE, drt/DRT_GLOBAL_SCOPE, drt/DRT_LINK_LOCAL_SCOPE, drt/DRT_SCOPE, drt/DRT_SITE_LOCAL_SCOPE, p2p.drt_scope
ms.topic: enum
f1_keywords: 
 - "drt/DRT_SCOPE"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_SCOPE
targetos: Windows
req.typenames: DRT_SCOPE
req.redist: 
ms.custom: 19H1
---

# DRT_SCOPE enumeration


## -description


The <b>DRT_SCOPE</b> enumeration defines the set of IPv6 scopes in which DRT operates while using the IPv6 UDP transport created by <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport">DrtCreateIpv6UdpTransport</a>.


## -enum-fields




### -field DRT_GLOBAL_SCOPE

Uses the global scope.


### -field DRT_SITE_LOCAL_SCOPE

The <b>DRT_SITE_LOCAL_SCOPE</b> has been deprecated and should not be used.


### -field DRT_LINK_LOCAL_SCOPE

Uses the link local scope.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport">DrtCreateIpv6UdpTransport</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver">DrtCreatePnrpBootstrapResolver</a>
 

 

