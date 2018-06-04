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

# AddConnectNotify function


## -description


The <b>AddConnectNotify</b> function is called before and after each add connection operation (<a href="https://msdn.microsoft.com/9f2cf166-eb08-4498-8cda-79808776a452">WNetAddConnection</a>, 
<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>, and 
<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>) is attempted by the <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Multiple Provider Router</a> (MPR).

The <b>AddConnectNotify</b> function is not called when MPR is automatically restoring network connections.


## -parameters




### -param lpNotifyInfo [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/43b31128-da9c-470b-b030-0010b250a291">NOTIFYINFO</a> structure that contains information about the notification.


### -param lpAddInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/23698bd9-12f6-4c1f-b833-bd5fddeba048">NOTIFYADD</a> structure that contains information about the connection being added.


## -returns




						If the function succeeds, the function should return WN_SUCCESS.

If the function fails, it should return an error code. This can be any of the error codes specified in 
<a href="https://msdn.microsoft.com/f8e6692f-4824-40fe-a5b3-9843689ea02e">Network Security Return Values</a>.




## -remarks



The <b>AddConnectNotify</b> function is implemented by applications that need to receive notification from the MPR when a network resource is connected or disconnected. For more information about how to write an application that receives such notifications, see 
<a href="https://msdn.microsoft.com/692eb8f2-1c53-4535-b44d-babb30eecd9c">Receiving Connection Notifications</a>.




## -see-also




<a href="https://msdn.microsoft.com/94bd969d-f94d-449c-971d-d17fff2c07e1">CancelConnectNotify</a>
 

 

