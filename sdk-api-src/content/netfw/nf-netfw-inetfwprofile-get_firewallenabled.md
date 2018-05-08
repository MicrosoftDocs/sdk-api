---
UID: NF:netfw.INetFwProfile.get_FirewallEnabled
title: INetFwProfile::get_FirewallEnabled
author: windows-driver-content
description: Indicates whether the firewall is enabled.
old-location: ics\inetfwprofile_firewallenabled.htm
old-project: ICS
ms.assetid: cde6327d-e3ae-418f-9e8c-76288c120ca0
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: FirewallEnabled property [ICS/ICF], FirewallEnabled property [ICS/ICF],INetFwProfile interface, INetFwProfile interface [ICS/ICF],FirewallEnabled property, INetFwProfile.FirewallEnabled, INetFwProfile.get_FirewallEnabled, INetFwProfile::FirewallEnabled, INetFwProfile::get_FirewallEnabled, INetFwProfile::put_FirewallEnabled, get_FirewallEnabled, ics.inetfwprofile_firewallenabled, netfw/INetFwProfile::FirewallEnabled, netfw/INetFwProfile::get_FirewallEnabled, netfw/INetFwProfile::put_FirewallEnabled
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
-	INetFwProfile.FirewallEnabled
-	INetFwProfile.get_FirewallEnabled
-	INetFwProfile.put_FirewallEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwProfile::get_FirewallEnabled


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the firewall is enabled.

This property is read/write.


## -parameters


## -remarks



 The resulting  firewall status is based on the local policy from the local store. Use the procedure <a href="https://msdn.microsoft.com/c2a6f57d-e05b-4143-90ad-39ca32d66c66">Checking the Effective Firewall Status</a> to determine the overall operational state. 




## -see-also




<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>
 

 

