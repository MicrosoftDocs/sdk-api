---
UID: NF:netfw.INetFwOpenPort.get_BuiltIn
title: INetFwOpenPort::get_BuiltIn
author: windows-driver-content
description: Indicates whether the port is defined by the system.
old-location: ics\inetfwopenport_builtin.htm
old-project: ICS
ms.assetid: 7260b9f2-2cbe-4b71-8c99-1d1c30870ae1
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: BuiltIn property [ICS/ICF], BuiltIn property [ICS/ICF],INetFwOpenPort interface, INetFwOpenPort interface [ICS/ICF],BuiltIn property, INetFwOpenPort.BuiltIn, INetFwOpenPort.get_BuiltIn, INetFwOpenPort::BuiltIn, INetFwOpenPort::get_BuiltIn, get_BuiltIn, ics.inetfwopenport_builtin, netfw/INetFwOpenPort::BuiltIn, netfw/INetFwOpenPort::get_BuiltIn
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
-	INetFwOpenPort.BuiltIn
-	INetFwOpenPort.get_BuiltIn
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwOpenPort::get_BuiltIn


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the port is defined by the system.

This property is read-only.


## -parameters


## -remarks



Ports  with their <b>BuiltIn</b> property set to true (<b>VARIANT_TRUE</b>) are system specified and cannot be removed, only the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>, <a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">RemoteAddress</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/dn915814">Scope</a> properties can be modified.




## -see-also




<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>
 

 

