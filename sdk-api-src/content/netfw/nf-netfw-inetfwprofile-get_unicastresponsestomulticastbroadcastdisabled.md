---
UID: NF:netfw.INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled
title: INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled
author: windows-sdk-content
description: Indicates whether the firewall should not allow unicast responses to multicast and broadcast traffic.
old-location: ics\inetfwprofile_unicastresponsestomulticastbroadcastdisabled.htm
tech.root: ICS
ms.assetid: 61a0c65e-8dfa-4f3e-a28f-141a72065123
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetFwProfile interface [ICS/ICF],UnicastResponsesToMulticastBroadcastDisabled property, INetFwProfile.UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled, UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF], UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF],INetFwProfile interface, get_UnicastResponsesToMulticastBroadcastDisabled, ics.inetfwprofile_unicastresponsestomulticastbroadcastdisabled, netfw/INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled, netfw/INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled, netfw/INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled
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
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwProfile.UnicastResponsesToMulticastBroadcastDisabled
 - INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled
 - INetFwProfile.put_UnicastResponsesToMulticastBroadcastDisabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- netfw.h
: 
- INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled
: 
---

# INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the firewall should not allow unicast responses to multicast and
   broadcast traffic.

This property is read/write.


## -parameters


## -remarks



If a PC sends a broadcast packet, a unicast response is allowed for three seconds. Use this property to change this behavior.




## -see-also




<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>
 

 

