---
UID: NF:netfw.INetFwRemoteAdminSettings.put_Scope
title: INetFwRemoteAdminSettings::put_Scope
author: windows-sdk-content
description: Controls the network scope from which remote administration is allowed.
old-location: ics\inetfwremoteadminsettings_scope.htm
old-project: ics
ms.assetid: 0ba9e6d1-82a4-4a58-9da0-0e07e79b0030
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INetFwRemoteAdminSettings interface [ICS/ICF],Scope property, INetFwRemoteAdminSettings.Scope, INetFwRemoteAdminSettings.put_Scope, INetFwRemoteAdminSettings::Scope, INetFwRemoteAdminSettings::get_Scope, INetFwRemoteAdminSettings::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF],INetFwRemoteAdminSettings interface, ics.inetfwremoteadminsettings_scope, netfw/INetFwRemoteAdminSettings::Scope, netfw/INetFwRemoteAdminSettings::get_Scope, netfw/INetFwRemoteAdminSettings::put_Scope, put_Scope
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
 - INetFwRemoteAdminSettings.Scope
 - INetFwRemoteAdminSettings.get_Scope
 - INetFwRemoteAdminSettings.put_Scope
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRemoteAdminSettings::put_Scope


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Controls the network scope from which remote administration is allowed.

This property is read/write.


## -parameters


## -remarks



When setting the
   <b>Scope</b> property, only <b>NET_FW_SCOPE_ALL</b> and <b>NET_FW_SCOPE_LOCAL_SUBNET</b> are valid.
   

The default value is
   <b>NET_FW_SCOPE_ALL</b> for new ports.

To create a custom scope, use the <a href="https://msdn.microsoft.com/9166617b-3e61-4d83-bd2f-92682ea5df82">RemoteAddresses</a> property of this interface.




## -see-also




<a href="https://msdn.microsoft.com/35f34a53-e73b-48be-ac79-9b7ab825c6ad">INetFwRemoteAdminSettings</a>



<a href="https://msdn.microsoft.com/71f52d88-efd3-4037-86bc-7ec1cfa9642f">NET_FW_SCOPE</a>



<a href="https://msdn.microsoft.com/9166617b-3e61-4d83-bd2f-92682ea5df82">RemoteAddresses</a>
 

 

