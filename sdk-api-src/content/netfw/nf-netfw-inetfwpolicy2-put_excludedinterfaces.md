---
UID: NF:netfw.INetFwPolicy2.put_ExcludedInterfaces
title: INetFwPolicy2::put_ExcludedInterfaces method
author: windows-driver-content
description: Specifies a list of interfaces on which firewall settings are excluded.
old-location: ics\inetfwpolicy2_excludedinterfaces.htm
old-project: ICS
ms.assetid: 0e8cbb09-c146-42e9-9b7c-002e6775bf19
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: ExcludedInterfaces property [ICS/ICF], ExcludedInterfaces property [ICS/ICF], INetFwPolicy2 interface, INetFwPolicy2, INetFwPolicy2 interface [ICS/ICF], ExcludedInterfaces property, INetFwPolicy2.ExcludedInterfaces, INetFwPolicy2::get_ExcludedInterfaces, INetFwPolicy2::put_ExcludedInterfaces, ics.inetfwpolicy2_excludedinterfaces, netfw/INetFwPolicy2::ExcludedInterfaces, netfw/INetFwPolicy2::get_ExcludedInterfaces, netfw/INetFwPolicy2::put_ExcludedInterfaces, put_ExcludedInterfaces,INetFwPolicy2.put_ExcludedInterfaces
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
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
api_name:
-	INetFwPolicy2.ExcludedInterfaces
-	INetFwPolicy2.get_ExcludedInterfaces
-	INetFwPolicy2.put_ExcludedInterfaces
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwPolicy2::put_ExcludedInterfaces method


## -description


Specifies a list of interfaces on which firewall settings are excluded.

This property is read/write.


## -parameters


## -remarks



An excluded interface is an interface to which the firewall is not applicable.  The firewall is not applicable to any traffic received from or sent to an excluded interface. An empty list indicates that there are no excluded interfaces.

When you pass a profile type obtained from the <a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_ExcludedInterfaces</b> and <b>put_ExcludedInterfaces</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.




## -see-also




<a href="https://msdn.microsoft.com/ef01a531-ddb0-4eb4-894b-82f613016396">INetFwPolicy2</a>
 

 

