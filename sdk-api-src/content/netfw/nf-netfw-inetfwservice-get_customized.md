---
UID: NF:netfw.INetFwService.get_Customized
title: INetFwService::get_Customized (netfw.h)
description: Indicates whether at least one of the ports associated with the service has been customized.
helpviewer_keywords: ["Customized property [ICS/ICF]","Customized property [ICS/ICF]","INetFwService interface","INetFwService interface [ICS/ICF]","Customized property","INetFwService.Customized","INetFwService.get_Customized","INetFwService::Customized","INetFwService::get_Customized","get_Customized","ics.inetfwservice_customized","netfw/INetFwService::Customized","netfw/INetFwService::get_Customized"]
old-location: ics\inetfwservice_customized.htm
tech.root: ics
ms.assetid: 6c26863a-b0eb-4e5a-b3a9-0129ab9a4df2
ms.date: 12/05/2018
ms.keywords: Customized property [ICS/ICF], Customized property [ICS/ICF],INetFwService interface, INetFwService interface [ICS/ICF],Customized property, INetFwService.Customized, INetFwService.get_Customized, INetFwService::Customized, INetFwService::get_Customized, get_Customized, ics.inetfwservice_customized, netfw/INetFwService::Customized, netfw/INetFwService::get_Customized
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
 - INetFwService::get_Customized
 - netfw/INetFwService::get_Customized
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
 - INetFwService.Customized
 - INetFwService.get_Customized
---

# INetFwService::get_Customized


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether at least one of the ports associated with the service
   has been customized.

This property is read-only.

## -parameters

## -remarks

If a service has been customized, the values
   returned by the service properties do not reflect the configuration of
   all the ports associated with the service.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a>