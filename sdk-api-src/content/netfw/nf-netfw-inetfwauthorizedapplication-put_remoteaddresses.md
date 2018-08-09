---
UID: NF:netfw.INetFwAuthorizedApplication.put_RemoteAddresses
title: INetFwAuthorizedApplication::put_RemoteAddresses
author: windows-sdk-content
description: Specifies a set of the remote addresses from which the application can listen for traffic.
old-location: ics\inetfwauthorizedapplication_remoteaddresses.htm
old-project: ics
ms.assetid: 56e51590-8cde-4c7d-8034-bc13f16f2617
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],RemoteAddresses property, INetFwAuthorizedApplication.RemoteAddresses, INetFwAuthorizedApplication.put_RemoteAddresses, INetFwAuthorizedApplication::RemoteAddresses, INetFwAuthorizedApplication::get_RemoteAddresses, INetFwAuthorizedApplication::put_RemoteAddresses, RemoteAddresses property [ICS/ICF], RemoteAddresses property [ICS/ICF],INetFwAuthorizedApplication interface, ics.inetfwauthorizedapplication_remoteaddresses, netfw/INetFwAuthorizedApplication::RemoteAddresses, netfw/INetFwAuthorizedApplication::get_RemoteAddresses, netfw/INetFwAuthorizedApplication::put_RemoteAddresses, put_RemoteAddresses
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
 - INetFwAuthorizedApplication.RemoteAddresses
 - INetFwAuthorizedApplication.get_RemoteAddresses
 - INetFwAuthorizedApplication.put_RemoteAddresses
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwAuthorizedApplication::put_RemoteAddresses


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies a set  of the remote addresses from which the application can listen for traffic.

This property is read/write.


## -parameters


## -remarks



The <i>remoteAddrs</i> parameter consists of one or more comma-delimited tokens specifying the remote addresses from which the application can listen for traffic. The default value is "*". 

Valid tokens:


<ul>
<li>"*": any remote address; if present, it must be the only token.</li>
<li>"LocalSubnet": not case-sensitive; specifying more than once has no effect.</li>
<li>subnet: may be specified using either subnet mask or network prefix notation. If neither a subnet mask nor a network prefix is specified, the subnet mask defaults to 255.255.255.255. Examples of valid subnets: 
10.0.0.2/255.0.0.0 
10.0.0.2/8 
10.0.0.2</li>
<li>Windows Vista: A valid IPv6 address.</li>
<li>Windows Vista: An IPv4 address range in the format "start address - end address."</li>
<li>Windows Vista: An IPv6 address range in the format "start address - end address."</li>
</ul>
For a predefined address range, use the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915814">Scope</a> property.




## -see-also




<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a>
 

 

