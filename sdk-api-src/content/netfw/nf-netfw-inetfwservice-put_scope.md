---
UID: NF:netfw.INetFwService.put_Scope
title: INetFwService::put_Scope
author: windows-sdk-content
description: Controls the network scope from which the port can listen.
old-location: ics\inetfwservice_scope.htm
old-project: ics
ms.assetid: 17a7e47d-2145-4439-9999-7384de9fd12c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwService interface [ICS/ICF],Scope property, INetFwService.Scope, INetFwService.put_Scope, INetFwService::Scope, INetFwService::get_Scope, INetFwService::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF],INetFwService interface, ics.inetfwservice_scope, netfw/INetFwService::Scope, netfw/INetFwService::get_Scope, netfw/INetFwService::put_Scope, put_Scope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.redist: 
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
 - INetFwService.Scope
 - INetFwService.get_Scope
 - INetFwService.put_Scope
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwService::put_Scope


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Controls the network scope from which the port can listen.

This property is read/write.


## -parameters


## -remarks



When setting the
   Scope property, only <b>NET_FW_SCOPE_ALL</b> and <b>NET_FW_SCOPE_LOCAL_SUBNET</b> are valid.
   

The default value is
   <b>NET_FW_SCOPE_ALL</b> for new ports.

To create a custom scope, use the <a href="https://msdn.microsoft.com/6cb1dfa1-1e92-47a8-9a97-45443f487f6e">RemoteAddresses</a> property.




## -see-also




<a href="https://msdn.microsoft.com/35f34a53-e73b-48be-ac79-9b7ab825c6ad">INetFwRemoteAdminSettings</a>



<a href="https://msdn.microsoft.com/57a777a4-03f5-416a-ae28-474d8794a759">INetFwService</a>



<a href="https://msdn.microsoft.com/6cb1dfa1-1e92-47a8-9a97-45443f487f6e">INetFwService.RemoteAddresses</a>



<a href="https://msdn.microsoft.com/71f52d88-efd3-4037-86bc-7ec1cfa9642f">NET_FW_SCOPE</a>
 

 

