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

# WTSEnumerateSessionsA function


## -description


Retrieves a list of sessions on a Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

A handle to the RD Session Host server.

<div class="alert"><b>Note</b>  You can use the 
<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> or <a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a> functions to retrieve a handle to a specific server, or  <b>WTS_CURRENT_SERVER_HANDLE</b> to use the RD Session Host server that hosts your application.</div>
<div> </div>

### -param Reserved [in]

This parameter is reserved. It must be zero.


### -param Version [in]

The version of the enumeration request. This parameter must be 1.


### -param ppSessionInfo [out]

A pointer to an array of <a href="https://msdn.microsoft.com/bb40d928-293a-4e2c-b7cf-2ac038da53c2">WTS_SESSION_INFO</a> structures that represent the retrieved sessions. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function.

<b>Session permissions:  </b><ul>
<li>To enumerate a session, you must enable the query information permission. For more information, see 
<a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a>.</li>
<li>To change permissions on a session, use the Remote Desktop Services Configuration administrative tool.</li>
<li>To enumerate sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.</li>
</ul>



### -param pCount [out]

A pointer to the number of 
<b>WTS_SESSION_INFO</b> structures returned in the <i>ppSessionInfo</i> parameter.


## -returns



Returns zero if this function fails. If this function succeeds, a nonzero value is returned.

To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more information, and an extended example on how to use this function, see the following <a href="https://support.microsoft.com/en-us/kb/291789">kb article</a>.




## -see-also




<a href="https://msdn.microsoft.com/bb40d928-293a-4e2c-b7cf-2ac038da53c2">WTS_SESSION_INFO</a>
 

 

