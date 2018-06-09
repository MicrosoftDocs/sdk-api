---
UID: NF:netfw.INetFwService.get_Customized
title: INetFwService::get_Customized
author: windows-sdk-content
description: Indicates whether at least one of the ports associated with the service has been customized.
old-location: ics\inetfwservice_customized.htm
old-project: ICS
ms.assetid: 6c26863a-b0eb-4e5a-b3a9-0129ab9a4df2
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: Customized property [ICS/ICF], Customized property [ICS/ICF],INetFwService interface, INetFwService interface [ICS/ICF],Customized property, INetFwService.Customized, INetFwService.get_Customized, INetFwService::Customized, INetFwService::get_Customized, get_Customized, ics.inetfwservice_customized, netfw/INetFwService::Customized, netfw/INetFwService::get_Customized
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwService::get_Customized


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether at least one of the ports associated with the service
   has been customized.

This property is read-only.


## -parameters


## -remarks



If a service has been customized, the values
   returned by the service properties do not reflect the configuration of
   all the ports associated with the service.




## -see-also




<a href="https://msdn.microsoft.com/57a777a4-03f5-416a-ae28-474d8794a759">INetFwService</a>
 

 

