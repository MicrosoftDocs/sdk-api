---
UID: NN:netfw.INetFwAuthorizedApplication
title: INetFwAuthorizedApplication (netfw.h)
description: The INetFwAuthorizedApplication interface provides access to the properties of an application that has been authorized have openings in the firewall.
helpviewer_keywords: ["INetFwAuthorizedApplication","INetFwAuthorizedApplication interface [ICS/ICF]","INetFwAuthorizedApplication interface [ICS/ICF]","described","ics.inetfwauthorizedapplication","netfw/INetFwAuthorizedApplication"]
old-location: ics\inetfwauthorizedapplication.htm
tech.root: ics
ms.assetid: 1ddeeab8-b81b-4d34-9ca6-103147fb3426
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplication, INetFwAuthorizedApplication interface [ICS/ICF], INetFwAuthorizedApplication interface [ICS/ICF],described, ics.inetfwauthorizedapplication, netfw/INetFwAuthorizedApplication
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
 - INetFwAuthorizedApplication
 - netfw/INetFwAuthorizedApplication
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
 - INetFwAuthorizedApplication
---

# INetFwAuthorizedApplication interface


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwAuthorizedApplication</b> interface provides access to the properties of an application that has been authorized have openings in the firewall.

## -inheritance

The <b>INetFwAuthorizedApplication</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwAuthorizedApplication</b> also has these types of members:

## -remarks

When creating new applications, this interface is supported by the HNetCfg.FwAuthorizedApplication COM object.  

For reading or modifying existing applications, instances of this interface are retrieved through the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a> collection.

All configuration changes take effect immediately.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
