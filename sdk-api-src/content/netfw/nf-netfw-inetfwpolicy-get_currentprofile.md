---
UID: NF:netfw.INetFwPolicy.get_CurrentProfile
title: INetFwPolicy::get_CurrentProfile
author: windows-driver-content
description: Retrieves the current firewall profile.
old-location: ics\inetfwpolicy_currentprofile.htm
old-project: ICS
ms.assetid: 2ee59a3e-a4e3-4714-aba7-9d72bfacfb34
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: CurrentProfile property [ICS/ICF], CurrentProfile property [ICS/ICF],INetFwPolicy interface, INetFwPolicy interface [ICS/ICF],CurrentProfile property, INetFwPolicy.CurrentProfile, INetFwPolicy.get_CurrentProfile, INetFwPolicy::CurrentProfile, INetFwPolicy::get_CurrentProfile, get_CurrentProfile, ics.inetfwpolicy_currentprofile, netfw/INetFwPolicy::CurrentProfile, netfw/INetFwPolicy::get_CurrentProfile
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
-	INetFwPolicy.CurrentProfile
-	INetFwPolicy.get_CurrentProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwPolicy::get_CurrentProfile


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Retrieves the current firewall profile.

This property is read-only.


## -parameters


## -remarks



The SharedAccess service must be running.

To get specific profile objects, use <a href="https://msdn.microsoft.com/4c3876cf-40a4-4315-a87a-8fcdf509d48e">INetFwPolicy::GetProfileByType</a> instead of <b>INetFwPolicy::CurrentProfile</b>.

On Windows 7, the netsh context <b>current</b> maps to all currently active profiles for netsh advfirewall and netsh firewall. On earlier versions of Windows, <b>current</b> maps to the most restrictive profile.




## -see-also




<a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a>



<a href="https://msdn.microsoft.com/8bfe55b6-c38d-47f8-9160-a304a85eb67f">INetFwPolicy</a>



<a href="https://msdn.microsoft.com/694bbff5-003d-4dde-9a85-f81ca29e6208">INetFwProfile</a>
 

 

