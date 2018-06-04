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

# IBDA_UserActivityService::UserActivityDetected


## -description


Indicates that a Media Sink Device (MSD) in a Protected Broadcast Driver Architecture (PBDA) media graph has detected user activity and is informing a Media Transfer Device (MTD) of this activity. The MSD calls this method only if the current activity interval has elapsed since the the MSD most recently called this method. The <a href="https://msdn.microsoft.com/2ea3504a-a479-4d26-8a6b-0e5bdddf6a21">GetUserActivityInterval</a> method sets or obtains the value of the current activity interval. 


## -parameters






## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
User activity service failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2ea3504a-a479-4d26-8a6b-0e5bdddf6a21">GetUserActivityInterval</a>



<a href="https://msdn.microsoft.com/d2c8f14e-11d7-4385-a6c8-31b086ec1286">IBDA_UserActivityService</a>
 

 

