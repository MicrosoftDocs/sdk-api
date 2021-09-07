---
UID: NN:netfw.INetFwOpenPort
title: INetFwOpenPort (netfw.h)
description: The INetFwOpenPort interface provides access to the properties of a port that has been opened in the firewall.
helpviewer_keywords: ["INetFwOpenPort","INetFwOpenPort interface [ICS/ICF]","INetFwOpenPort interface [ICS/ICF]","described","ics.inetfwopenport","netfw/INetFwOpenPort"]
old-location: ics\inetfwopenport.htm
tech.root: ics
ms.assetid: 1a9fd676-b1c0-4be5-9571-d14ac5980af5
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort, INetFwOpenPort interface [ICS/ICF], INetFwOpenPort interface [ICS/ICF],described, ics.inetfwopenport, netfw/INetFwOpenPort
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
 - INetFwOpenPort
 - netfw/INetFwOpenPort
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
 - INetFwOpenPort
---

# INetFwOpenPort interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwOpenPort</b> interface provides access to the properties of a port that has been opened in the firewall.

## -inheritance

The <b>INetFwOpenPort</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwOpenPort</b> also has these types of members:

## -remarks

Ports  with their <b>BuiltIn</b> property set to true (<b>VARIANT_TRUE</b>) are system specified and cannot be removed.

When creating new ports, this interface is supported by the
<b>HNetCfg.FWOpenPort</b> COM object. 

For reading or modifying existing ports,
instances of this interface are retrieved through the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a> collection. 

All configuration changes take effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
