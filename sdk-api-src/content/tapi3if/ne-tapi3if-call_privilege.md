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

# CALL_PRIVILEGE enumeration


## -description


A 
<b>CALL_PRIVILEGE</b> member is returned by the 
<a href="https://msdn.microsoft.com/64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53">ITCallInfo::get_Privilege</a> method, and indicates when the current application owns or is monitoring the current call.


## -enum-fields




### -field CP_OWNER

The application is the owner of the call.


### -field CP_MONITOR

The application is a monitor of the call.


## -see-also




<a href="https://msdn.microsoft.com/64a80fb6-b5bc-45c5-9f1d-a89ac95b9c53">ITCallInfo::get_Privilege</a>
 

 

