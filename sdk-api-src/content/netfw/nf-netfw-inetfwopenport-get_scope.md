---
UID: NF:netfw.INetFwOpenPort.get_Scope
title: INetFwOpenPort::get_Scope method
author: windows-driver-content
description: Controls the network scope from which the port can listen.
old-location: ics\inetfwopenport_scope.htm
old-project: ICS
ms.assetid: a5bd787f-e00c-4a57-adc7-a9618809198a
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: INetFwOpenPort, INetFwOpenPort interface [ICS/ICF], Scope property, INetFwOpenPort.Scope, INetFwOpenPort::get_Scope, INetFwOpenPort::put_Scope, Scope property [ICS/ICF], Scope property [ICS/ICF], INetFwOpenPort interface, get_Scope,INetFwOpenPort.get_Scope, ics.inetfwopenport_scope, netfw/INetFwOpenPort::Scope, netfw/INetFwOpenPort::get_Scope, netfw/INetFwOpenPort::put_Scope
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
-	Hnetcfg.dll
api_name:
-	INetFwOpenPort.Scope
-	INetFwOpenPort.get_Scope
-	INetFwOpenPort.put_Scope
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwOpenPort::get_Scope method


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

To create a custom scope, use the <a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">RemoteAddresses</a> property.




## -see-also




<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>



<a href="https://msdn.microsoft.com/35f34a53-e73b-48be-ac79-9b7ab825c6ad">INetFwRemoteAdminSettings</a>



<a href="https://msdn.microsoft.com/71f52d88-efd3-4037-86bc-7ec1cfa9642f">NET_FW_SCOPE</a>
 

 

