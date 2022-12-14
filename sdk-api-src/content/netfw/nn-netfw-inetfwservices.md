---
UID: NN:netfw.INetFwServices
title: INetFwServices (netfw.h)
description: The INetFwServices interface is a standard Automation interface which provides access to a collection of services that may be authorized to listen through the firewall.
helpviewer_keywords: ["INetFwServices","INetFwServices interface [ICS/ICF]","INetFwServices interface [ICS/ICF]","described","ics.inetfwservices","netfw/INetFwServices"]
old-location: ics\inetfwservices.htm
tech.root: ics
ms.assetid: b99464c5-dabc-405a-ad3e-da06a6faef47
ms.date: 12/05/2018
ms.keywords: INetFwServices, INetFwServices interface [ICS/ICF], INetFwServices interface [ICS/ICF],described, ics.inetfwservices, netfw/INetFwServices
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
 - INetFwServices
 - netfw/INetFwServices
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
 - INetFwServices
---

# INetFwServices interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwServices</b> interface is a standard Automation interface which provides access to a collection of services that may be authorized to listen
through the firewall.

## -inheritance

The <b>INetFwServices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwServices</b> also has these types of members:

## -remarks

An instance of this interface is retrieved through the
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">Services</a> property of the INetFwProfile interface. 

All configuration
changes take effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">INetFwProfile.Services</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
