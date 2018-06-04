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

# IMMDeviceEnumerator::UnregisterEndpointNotificationCallback


## -description



The <b>UnregisterEndpointNotificationCallback</b> method deletes the registration of a notification interface that the client registered in a previous call to the <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.




## -parameters




### -param pClient






#### - pNotify [in]

Pointer to the client's <a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient</a> interface. The client passed this same interface pointer to the device enumerator in a previous call to the <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pNotify</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified notification interface was not found.

</td>
</tr>
</table>
 




## -remarks




        
      The client must ensure that the <a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient</a> object is not released after the <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">RegisterEndpointNotificationCallback</a> call and before calling <b>UnregisterEndpointNotificationCallback</b>. These methods do not call the client's <b>IMMNotificationClient::AddRef</b> and <b>IMMNotificationClient::Release</b> implementations. The client is responsible for maintaining the reference count of the <b>IMMNotificationClient</b> object. The client must increment the count if the <b>RegisterEndpointNotificationCallback</b> call succeeds and release the final reference only after calling <b>UnregisterEndpointNotificationCallback</b> or implement some other mechanism to ensure that the object is not deleted before <b>UnregisterEndpointNotificationCallback</b> is called. Otherwise, the application leaks the resources held by the <b>IMMNotificationClient</b> and any other object that is implemented in the same container. 



For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <b>IUnknown</b> interface in the Windows SDK documentation.





## -see-also




<a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>



<a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a>



<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

