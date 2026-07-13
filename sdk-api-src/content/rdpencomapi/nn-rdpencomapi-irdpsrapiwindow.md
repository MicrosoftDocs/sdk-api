---
UID: NN:rdpencomapi.IRDPSRAPIWindow
title: IRDPSRAPIWindow (rdpencomapi.h)
description: Represents a one-to-one mapping to a sharable window.
helpviewer_keywords: ["IRDPSRAPIWindow","IRDPSRAPIWindow interface [RDP]","IRDPSRAPIWindow interface [RDP]","described","rdp.irdpsrapiwindow","rdpencomapi/IRDPSRAPIWindow"]
old-location: rdp\irdpsrapiwindow.htm
tech.root: rdp
ms.assetid: 85c8263b-e796-4748-b8e5-6315e5937861
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIWindow, IRDPSRAPIWindow interface [RDP], IRDPSRAPIWindow interface [RDP],described, rdp.irdpsrapiwindow, rdpencomapi/IRDPSRAPIWindow
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
 - IRDPSRAPIWindow
 - rdpencomapi/IRDPSRAPIWindow
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
 - IRDPSRAPIWindow
---

# IRDPSRAPIWindow interface


## -description

Represents a one-to-one mapping to a sharable window. A sharable window is usually a top-level window that does not have an owner. Sharing the content of a window can be enabled or disabled by setting the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiwindow-get_shared">Shared</a> property on the window object to <b>TRUE</b> or <b>FALSE</b>. Applications can use this window object to display a list of windows that can be shared.

## -inheritance

The <b>IRDPSRAPIWindow</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIWindow</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiwindowlist">IRDPSRAPIWindowList</a>
