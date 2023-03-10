---
UID: NF:netfw.INetFwOpenPort.get_Scope
title: INetFwOpenPort::get_Scope (netfw.h)
description: Controls the network scope from which the port can listen. (INetFwOpenPort.get_Scope)
helpviewer_keywords: ["INetFwOpenPort interface [ICS/ICF]","Scope property","INetFwOpenPort.Scope","INetFwOpenPort.get_Scope","INetFwOpenPort::Scope","INetFwOpenPort::get_Scope","INetFwOpenPort::put_Scope","Scope property [ICS/ICF]","Scope property [ICS/ICF]","INetFwOpenPort interface","get_Scope","ics.inetfwopenport_scope","netfw/INetFwOpenPort::Scope","netfw/INetFwOpenPort::get_Scope","netfw/INetFwOpenPort::put_Scope"]
old-location: ics\inetfwopenport_scope.htm
tech.root: ics
ms.assetid: a5bd787f-e00c-4a57-adc7-a9618809198a
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],Scope property, INetFwOpenPort.Scope, INetFwOpenPort.get_Scope, INetFwOpenPort::Scope, INetFwOpenPort::get_Scope, INetFwOpenPort::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF],INetFwOpenPort interface, get_Scope, ics.inetfwopenport_scope, netfw/INetFwOpenPort::Scope, netfw/INetFwOpenPort::get_Scope, netfw/INetFwOpenPort::put_Scope
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
 - INetFwOpenPort::get_Scope
 - netfw/INetFwOpenPort::get_Scope
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
 - INetFwOpenPort.Scope
 - INetFwOpenPort.get_Scope
 - INetFwOpenPort.put_Scope
---

# INetFwOpenPort::get_Scope


## -description

<p class="CCE_Message">[The Windows Firewall API is > [!NOTE]
> The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the [Windows Firewall with Advanced Security](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page) API is recommended.

Controls the network scope from which the port can listen.

This property is read/write.

## -parameters

## -remarks

When setting the
   Scope property, only <b>NET_FW_SCOPE_ALL</b> and <b>NET_FW_SCOPE_LOCAL_SUBNET</b> are valid.

The default value is
   <b>NET_FW_SCOPE_ALL</b> for new ports.

To create a custom scope, use the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_remoteaddresses">RemoteAddresses</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>


<a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_scope">NET_FW_SCOPE</a>
