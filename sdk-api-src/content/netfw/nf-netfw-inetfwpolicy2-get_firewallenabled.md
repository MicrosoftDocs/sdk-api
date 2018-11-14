---
UID: NF:netfw.INetFwPolicy2.get_FirewallEnabled
title: INetFwPolicy2::get_FirewallEnabled
author: windows-sdk-content
description: Indicates whether a firewall is enabled locally (the effective result may differ due to group policy settings).
old-location: ics\inetfwpolicy2_firewallenabled.htm
tech.root: ICS
ms.assetid: 6c3ca9dd-a562-454f-bb9a-856beba772f3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FirewallEnabled property [ICS/ICF], FirewallEnabled property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],FirewallEnabled property, INetFwPolicy2.FirewallEnabled, INetFwPolicy2.get_FirewallEnabled, INetFwPolicy2::FirewallEnabled, INetFwPolicy2::get_FirewallEnabled, INetFwPolicy2::put_FirewallEnabled, get_FirewallEnabled, ics.inetfwpolicy2_firewallenabled, netfw/INetFwPolicy2::FirewallEnabled, netfw/INetFwPolicy2::get_FirewallEnabled, netfw/INetFwPolicy2::put_FirewallEnabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwPolicy2.FirewallEnabled
 - INetFwPolicy2.get_FirewallEnabled
 - INetFwPolicy2.put_FirewallEnabled
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
- INetFwPolicy2.get_FirewallEnabled
: 
---

# INetFwPolicy2::get_FirewallEnabled


## -description


Indicates whether a firewall is enabled locally (the effective result may differ due to group policy settings).

This property is read/write.


## -parameters


## -remarks



When you pass a profile type obtained from the <a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_FirewallEnabled</b> and <b>put_FirewallEnabled</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.




## -see-also




<a href="https://msdn.microsoft.com/ef01a531-ddb0-4eb4-894b-82f613016396">INetFwPolicy2</a>
 

 

