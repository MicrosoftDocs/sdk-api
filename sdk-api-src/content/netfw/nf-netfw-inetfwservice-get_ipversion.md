---
UID: NF:netfw.INetFwService.get_IpVersion
title: INetFwService::get_IpVersion (netfw.h)
description: Specifies the firewall IP version for which the service is authorized. (Get)
helpviewer_keywords: ["INetFwService interface [ICS/ICF]","IpVersion property","INetFwService.IpVersion","INetFwService.get_IpVersion","INetFwService::IpVersion","INetFwService::get_IpVersion","INetFwService::put_IpVersion","IpVersion property [ICS/ICF]","IpVersion property [ICS/ICF]","INetFwService interface","get_IpVersion","ics.inetfwservice_ipversion","netfw/INetFwService::IpVersion","netfw/INetFwService::get_IpVersion","netfw/INetFwService::put_IpVersion"]
old-location: ics\inetfwservice_ipversion.htm
tech.root: ics
ms.assetid: 992f39f6-ffb7-40c0-9227-6e626f226313
ms.date: 12/05/2018
ms.keywords: INetFwService interface [ICS/ICF],IpVersion property, INetFwService.IpVersion, INetFwService.get_IpVersion, INetFwService::IpVersion, INetFwService::get_IpVersion, INetFwService::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwService interface, get_IpVersion, ics.inetfwservice_ipversion, netfw/INetFwService::IpVersion, netfw/INetFwService::get_IpVersion, netfw/INetFwService::put_IpVersion
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
 - INetFwService::get_IpVersion
 - netfw/INetFwService::get_IpVersion
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
 - INetFwService.IpVersion
 - INetFwService.get_IpVersion
 - INetFwService.put_IpVersion
---

# INetFwService::get_IpVersion


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the firewall IP version  for which  the service is authorized.

This property is read/write.

## -parameters

## -remarks

Only
   <b>NET_FW_IP_VERSION_ANY</b> is supported.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_version">NET_FW_IP_VERSION</a>
