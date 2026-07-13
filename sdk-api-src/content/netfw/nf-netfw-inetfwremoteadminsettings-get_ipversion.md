---
UID: NF:netfw.INetFwRemoteAdminSettings.get_IpVersion
title: INetFwRemoteAdminSettings::get_IpVersion (netfw.h)
description: Specifies the IP version. (INetFwRemoteAdminSettings.get_IpVersion)
helpviewer_keywords: ["INetFwRemoteAdminSettings interface [ICS/ICF]","IpVersion property","INetFwRemoteAdminSettings.IpVersion","INetFwRemoteAdminSettings.get_IpVersion","INetFwRemoteAdminSettings::IpVersion","INetFwRemoteAdminSettings::get_IpVersion","INetFwRemoteAdminSettings::put_IpVersion","IpVersion property [ICS/ICF]","IpVersion property [ICS/ICF]","INetFwRemoteAdminSettings interface","get_IpVersion","ics.inetfwremoteadminsettings_ipversion","netfw/INetFwRemoteAdminSettings::IpVersion","netfw/INetFwRemoteAdminSettings::get_IpVersion","netfw/INetFwRemoteAdminSettings::put_IpVersion"]
old-location: ics\inetfwremoteadminsettings_ipversion.htm
tech.root: ics
ms.assetid: 55303549-84d7-42d1-b722-a281acd50648
ms.date: 12/05/2018
ms.keywords: INetFwRemoteAdminSettings interface [ICS/ICF],IpVersion property, INetFwRemoteAdminSettings.IpVersion, INetFwRemoteAdminSettings.get_IpVersion, INetFwRemoteAdminSettings::IpVersion, INetFwRemoteAdminSettings::get_IpVersion, INetFwRemoteAdminSettings::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwRemoteAdminSettings interface, get_IpVersion, ics.inetfwremoteadminsettings_ipversion, netfw/INetFwRemoteAdminSettings::IpVersion, netfw/INetFwRemoteAdminSettings::get_IpVersion, netfw/INetFwRemoteAdminSettings::put_IpVersion
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
 - INetFwRemoteAdminSettings::get_IpVersion
 - netfw/INetFwRemoteAdminSettings::get_IpVersion
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
 - INetFwRemoteAdminSettings.IpVersion
 - INetFwRemoteAdminSettings.get_IpVersion
 - INetFwRemoteAdminSettings.put_IpVersion
---

# INetFwRemoteAdminSettings::get_IpVersion


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version.

This property is read/write.

## -parameters

## -remarks

This is the IP version for which remote admin is authorized. 

Only
    <b>NET_FW_IP_VERSION_ANY</b> is supported.

## -see-also

<a href="/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_version">NET_FW_IP_VERSION</a>
