---
UID: NN:netfw.INetFwIcmpSettings
title: INetFwIcmpSettings (netfw.h)
description: The INetFwIcmpSettings interface provides access to the settings controlling ICMP packets.
helpviewer_keywords: ["INetFwIcmpSettings","INetFwIcmpSettings interface [ICS/ICF]","INetFwIcmpSettings interface [ICS/ICF]","described","ics.inetfwicmpsettings","netfw/INetFwIcmpSettings"]
old-location: ics\inetfwicmpsettings.htm
tech.root: ics
ms.assetid: 4eed8f30-4265-4735-a885-83c11b5031e5
ms.date: 12/05/2018
ms.keywords: INetFwIcmpSettings, INetFwIcmpSettings interface [ICS/ICF], INetFwIcmpSettings interface [ICS/ICF],described, ics.inetfwicmpsettings, netfw/INetFwIcmpSettings
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
 - INetFwIcmpSettings
 - netfw/INetFwIcmpSettings
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
 - INetFwIcmpSettings
---

# INetFwIcmpSettings interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwIcmpSettings</b> interface  provides access to the settings controlling ICMP packets.

## -inheritance

The <b>INetFwIcmpSettings</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwIcmpSettings</b> also has these types of members:

## -remarks

Instances of this interface
are retrieved through the <a href="/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">IcmpSettings</a> property of the INetFwProfile interface.

Because the methods and properties of this interface enable all rules belonging to a given ICMP type, enabling a rule may enable rules from other groups as well.

All configuration changes take
effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">INetFwProfile.IcmpSettings</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
