---
UID: NF:netfw.INetFwRemoteAdminSettings.put_Scope
title: INetFwRemoteAdminSettings::put_Scope (netfw.h)
description: Controls the network scope from which remote administration is allowed. (Put)
helpviewer_keywords: ["INetFwRemoteAdminSettings interface [ICS/ICF]","Scope property","INetFwRemoteAdminSettings.Scope","INetFwRemoteAdminSettings.put_Scope","INetFwRemoteAdminSettings::Scope","INetFwRemoteAdminSettings::get_Scope","INetFwRemoteAdminSettings::put_Scope","Scope property [ICS/ICF]","Scope property [ICS/ICF]","INetFwRemoteAdminSettings interface","ics.inetfwremoteadminsettings_scope","netfw/INetFwRemoteAdminSettings::Scope","netfw/INetFwRemoteAdminSettings::get_Scope","netfw/INetFwRemoteAdminSettings::put_Scope","put_Scope"]
old-location: ics\inetfwremoteadminsettings_scope.htm
tech.root: ics
ms.assetid: 0ba9e6d1-82a4-4a58-9da0-0e07e79b0030
ms.date: 12/05/2018
ms.keywords: INetFwRemoteAdminSettings interface [ICS/ICF],Scope property, INetFwRemoteAdminSettings.Scope, INetFwRemoteAdminSettings.put_Scope, INetFwRemoteAdminSettings::Scope, INetFwRemoteAdminSettings::get_Scope, INetFwRemoteAdminSettings::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF],INetFwRemoteAdminSettings interface, ics.inetfwremoteadminsettings_scope, netfw/INetFwRemoteAdminSettings::Scope, netfw/INetFwRemoteAdminSettings::get_Scope, netfw/INetFwRemoteAdminSettings::put_Scope, put_Scope
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
 - INetFwRemoteAdminSettings::put_Scope
 - netfw/INetFwRemoteAdminSettings::put_Scope
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
 - INetFwRemoteAdminSettings.Scope
 - INetFwRemoteAdminSettings.get_Scope
 - INetFwRemoteAdminSettings.put_Scope
---

# INetFwRemoteAdminSettings::put_Scope


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Controls the network scope from which remote administration is allowed.

This property is read/write.

## -parameters

## -remarks

When setting the
   <b>Scope</b> property, only <b>NET_FW_SCOPE_ALL</b> and <b>NET_FW_SCOPE_LOCAL_SUBNET</b> are valid.
   

The default value is
   <b>NET_FW_SCOPE_ALL</b> for new ports.

To create a custom scope, use the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_remoteaddresses">RemoteAddresses</a> property of this interface.

## -see-also

<a href="/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>




<a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_scope">NET_FW_SCOPE</a>


<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_remoteaddresses">RemoteAddresses</a>
