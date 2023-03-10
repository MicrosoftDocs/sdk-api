---
UID: NN:netfw.INetFwOpenPorts
title: INetFwOpenPorts (netfw.h)
description: The INetFwOpenPorts interface is a standard Automation collection interface.
helpviewer_keywords: ["INetFwOpenPorts","INetFwOpenPorts interface [ICS/ICF]","INetFwOpenPorts interface [ICS/ICF]","described","ics.inetfwopenports","netfw/INetFwOpenPorts"]
old-location: ics\inetfwopenports.htm
tech.root: ics
ms.assetid: a3a6e5c1-5818-419c-8df4-966b2fbcd8c0
ms.date: 12/05/2018
ms.keywords: INetFwOpenPorts, INetFwOpenPorts interface [ICS/ICF], INetFwOpenPorts interface [ICS/ICF],described, ics.inetfwopenports, netfw/INetFwOpenPorts
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwOpenPorts
 - netfw/INetFwOpenPorts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwOpenPorts
---

# INetFwOpenPorts interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwOpenPorts</b> interface is a standard Automation collection interface.

## -inheritance

The <b>INetFwOpenPorts</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwOpenPorts</b> also has these types of members:

## -remarks

An instance
of this interface is retrieved through the <a href="/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_globallyopenports">GloballyOpenPorts</a> property of the
INetFwProfile interface.

All configuration changes take effect
immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
