---
UID: NF:netfw.INetFwAuthorizedApplication.get_Scope
title: INetFwAuthorizedApplication::get_Scope (netfw.h)
description: Controls the network scope from which the port can listen.
helpviewer_keywords: ["INetFwAuthorizedApplication interface [ICS/ICF]","Scope property","INetFwAuthorizedApplication.Scope","INetFwAuthorizedApplication.get_Scope","INetFwAuthorizedApplication::Scope","INetFwAuthorizedApplication::get_Scope","INetFwAuthorizedApplication::put_Scope","Scope property [ICS/ICF]","Scope property [ICS/ICF]","INetFwAuthorizedApplication interface","get_Scope","ics.inetfwauthorizedapplication_scope","netfw/INetFwAuthorizedApplication::Scope","netfw/INetFwAuthorizedApplication::get_Scope","netfw/INetFwAuthorizedApplication::put_Scope"]
old-location: ics\inetfwauthorizedapplication_scope.htm
tech.root: ics
ms.assetid: f9784736-2af0-4bd4-980c-2365a1cdc20b
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],Scope property, INetFwAuthorizedApplication.Scope, INetFwAuthorizedApplication.get_Scope, INetFwAuthorizedApplication::Scope, INetFwAuthorizedApplication::get_Scope, INetFwAuthorizedApplication::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF],INetFwAuthorizedApplication interface, get_Scope, ics.inetfwauthorizedapplication_scope, netfw/INetFwAuthorizedApplication::Scope, netfw/INetFwAuthorizedApplication::get_Scope, netfw/INetFwAuthorizedApplication::put_Scope
f1_keywords:
- netfw/INetFwAuthorizedApplication.Scope
dev_langs:
- c++
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
req.dll: FirewallAPI.dll; Wfapi.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FirewallAPI.dll
- wfapi.dll
- Hnetcfg.dll
api_name:
- INetFwAuthorizedApplication.Scope
- INetFwAuthorizedApplication.get_Scope
- INetFwAuthorizedApplication.put_Scope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwAuthorizedApplication::get_Scope


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Controls the network scope from which the port can listen.

This property is read/write.


## -parameters


## -remarks



When setting the
   Scope property, only <b>NET_FW_SCOPE_ALL</b> and <b>NET_FW_SCOPE_LOCAL_SUBNET</b> are valid.
   

The default value is
   <b>NET_FW_SCOPE_ALL</b> for new ports.

To create a custom scope, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwauthorizedapplication-get_remoteaddresses">RemoteAddresses</a> property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFwAuthorizedApplication</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>



<a href="https://docs.microsoft.com/en-us/windows/win32/api/icftypes/ne-icftypes-net_fw_scope">NET_FW_SCOPE</a>
 

 

