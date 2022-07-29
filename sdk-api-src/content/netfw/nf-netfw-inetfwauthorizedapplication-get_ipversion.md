---
UID: NF:netfw.INetFwAuthorizedApplication.get_IpVersion
title: INetFwAuthorizedApplication::get_IpVersion (netfw.h)
description: Specifies the IP version setting for this application. (Get)
helpviewer_keywords: ["INetFwAuthorizedApplication interface [ICS/ICF]","IpVersion property","INetFwAuthorizedApplication.IpVersion","INetFwAuthorizedApplication.get_IpVersion","INetFwAuthorizedApplication::IpVersion","INetFwAuthorizedApplication::get_IpVersion","INetFwAuthorizedApplication::put_IpVersion","IpVersion property [ICS/ICF]","IpVersion property [ICS/ICF]","INetFwAuthorizedApplication interface","get_IpVersion","ics.inetfwauthorizedapplication_ipversion","netfw/INetFwAuthorizedApplication::IpVersion","netfw/INetFwAuthorizedApplication::get_IpVersion","netfw/INetFwAuthorizedApplication::put_IpVersion"]
old-location: ics\inetfwauthorizedapplication_ipversion.htm
tech.root: ics
ms.assetid: f0a4127f-4f81-4b71-a5c5-ba9e30927820
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],IpVersion property, INetFwAuthorizedApplication.IpVersion, INetFwAuthorizedApplication.get_IpVersion, INetFwAuthorizedApplication::IpVersion, INetFwAuthorizedApplication::get_IpVersion, INetFwAuthorizedApplication::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwAuthorizedApplication interface, get_IpVersion, ics.inetfwauthorizedapplication_ipversion, netfw/INetFwAuthorizedApplication::IpVersion, netfw/INetFwAuthorizedApplication::get_IpVersion, netfw/INetFwAuthorizedApplication::put_IpVersion
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
 - INetFwAuthorizedApplication::get_IpVersion
 - netfw/INetFwAuthorizedApplication::get_IpVersion
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
 - INetFwAuthorizedApplication.IpVersion
 - INetFwAuthorizedApplication.get_IpVersion
 - INetFwAuthorizedApplication.put_IpVersion
---

# INetFwAuthorizedApplication::get_IpVersion


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version  setting for this application.

This property is read/write.

## -parameters

## -remarks

Only <a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_version">NET_FW_IP_VERSION_ANY</a> is supported and this is the default for new applications.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFwAuthorizedApplication</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_version">NET_FW_IP_VERSION</a>
