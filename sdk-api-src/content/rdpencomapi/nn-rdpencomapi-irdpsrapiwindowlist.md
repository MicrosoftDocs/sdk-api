---
UID: NN:rdpencomapi.IRDPSRAPIWindowList
title: IRDPSRAPIWindowList (rdpencomapi.h)
description: Manages the window list.
helpviewer_keywords: ["IRDPSRAPIWindowList","IRDPSRAPIWindowList interface [RDP]","IRDPSRAPIWindowList interface [RDP]","described","rdp.irdpsrapiwindowlist","rdpencomapi/IRDPSRAPIWindowList"]
old-location: rdp\irdpsrapiwindowlist.htm
tech.root: rdp
ms.assetid: 9ea90838-6de3-4b21-8db8-ff96e026505a
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIWindowList, IRDPSRAPIWindowList interface [RDP], IRDPSRAPIWindowList interface [RDP],described, rdp.irdpsrapiwindowlist, rdpencomapi/IRDPSRAPIWindowList
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
 - IRDPSRAPIWindowList
 - rdpencomapi/IRDPSRAPIWindowList
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
 - IRDPSRAPIWindowList
---

# IRDPSRAPIWindowList interface


## -description

Manages the window list.

Applications obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplication-get_windows">IRDPSRAPIApplication::get_Windows</a> or <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplicationfilter-get_windows">IRDPSRAPIApplicationFilter::get_Windows</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiwindow">IRDPSRAPIWindow</a>