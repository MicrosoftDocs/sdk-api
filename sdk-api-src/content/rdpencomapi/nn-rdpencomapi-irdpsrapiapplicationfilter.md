---
UID: NN:rdpencomapi.IRDPSRAPIApplicationFilter
title: IRDPSRAPIApplicationFilter (rdpencomapi.h)
description: Manages the shared desktop area at the window and process level. Applications can use the enumerators to display lists of objects in the session that can be shared.
helpviewer_keywords: ["IRDPSRAPIApplicationFilter","IRDPSRAPIApplicationFilter interface [RDP]","IRDPSRAPIApplicationFilter interface [RDP]","described","rdp.irdpsrapiapplicationfilter","rdpencomapi/IRDPSRAPIApplicationFilter"]
old-location: rdp\irdpsrapiapplicationfilter.htm
tech.root: rdp
ms.assetid: 6a08c948-1b25-4a36-93c8-23e7e3f4fb08
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIApplicationFilter, IRDPSRAPIApplicationFilter interface [RDP], IRDPSRAPIApplicationFilter interface [RDP],described, rdp.irdpsrapiapplicationfilter, rdpencomapi/IRDPSRAPIApplicationFilter
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIApplicationFilter
 - rdpencomapi/IRDPSRAPIApplicationFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIApplicationFilter
---

# IRDPSRAPIApplicationFilter interface


## -description

Manages the shared desktop area at the window and process level. Applications can use the enumerators to display lists of objects in the session that can be shared.

Applications can obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_applicationfilter">IRDPSRAPISharingSession::ApplicationFilter</a>.

The list of sharable objects is exposed as a two-level tree. Each window has an application object as a parent. Each window object has its own sharing state that can be overridden by the sharing state of its parent. Each application object has its own sharing state that can be overridden by the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplicationfilter-get_enabled">Enabled</a> property of the application filter. Therefore, if an application filter is enabled and the application is shared, its windows are shared regardless of their sharing state. If the application filter is enabled but the application is not shared, its windows are shared depending on their sharing state.

If a shared application creates a new window that is sharable, it will be shared because the parent application is shared.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplication">IRDPSRAPIApplication</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplicationlist">IRDPSRAPIApplicationList</a>