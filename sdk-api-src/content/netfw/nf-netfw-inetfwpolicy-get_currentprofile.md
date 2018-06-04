---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

