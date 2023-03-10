---
UID: NN:netfw.INetFwProfile
title: INetFwProfile (netfw.h)
description: The INetFwProfile interface provides access to the firewall settings profile.
helpviewer_keywords: ["INetFwProfile","INetFwProfile interface [ICS/ICF]","INetFwProfile interface [ICS/ICF]","described","ics.inetfwprofile","netfw/INetFwProfile"]
old-location: ics\inetfwprofile.htm
tech.root: ics
ms.assetid: 694bbff5-003d-4dde-9a85-f81ca29e6208
ms.date: 12/05/2018
ms.keywords: INetFwProfile, INetFwProfile interface [ICS/ICF], INetFwProfile interface [ICS/ICF],described, ics.inetfwprofile, netfw/INetFwProfile
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
 - INetFwProfile
 - netfw/INetFwProfile
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
 - INetFwProfile
---

# INetFwProfile interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwProfile</b> interface  provides access to the firewall settings profile.

## -inheritance

The <b>INetFwProfile</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwProfile</b> also has these types of members:

## -remarks

Instances of this interface
are retrieved through the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-get_currentprofile">CurrentProfile</a> property or <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-getprofilebytype">GetProfileByType</a> method
of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy">INetFwPolicy</a> interface.

All configuration changes take
effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a>



<a href="/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservices">InetFwServices</a>
