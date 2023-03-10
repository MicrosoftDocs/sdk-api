---
UID: NN:sbtsv.ITsSbLoadBalancing
title: ITsSbLoadBalancing (sbtsv.h)
description: Exposes methods you can use to provide a custom load-balancing algorithm.
helpviewer_keywords: ["ITsSbLoadBalancing","ITsSbLoadBalancing interface [Remote Desktop Services]","ITsSbLoadBalancing interface [Remote Desktop Services]","described","sbtsv/ITsSbLoadBalancing","termserv.itssbloadbalancing"]
old-location: termserv\itssbloadbalancing.htm
tech.root: TermServ
ms.assetid: 2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancing, ITsSbLoadBalancing interface [Remote Desktop Services], ITsSbLoadBalancing interface [Remote Desktop Services],described, sbtsv/ITsSbLoadBalancing, termserv.itssbloadbalancing
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbLoadBalancing
 - sbtsv/ITsSbLoadBalancing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbLoadBalancing
---

# ITsSbLoadBalancing interface


## -description

Exposes methods you can use to provide a custom load-balancing algorithm.

The 
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbloadbalancing-getmostsuitabletarget">GetMostSuitableTarget</a> method should return an endpoint (target) to which the client 
connects.

## -inheritance

The <b>ITsSbLoadBalancing</b> interface inherits from <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbLoadBalancing</b> also has these types of members:

## -remarks

A plug-in can implement this interface to provide a custom load-balancing algorithm.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
