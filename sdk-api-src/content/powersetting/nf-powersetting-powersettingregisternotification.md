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

# PowerSettingRegisterNotification function


## -description


Registers to receive notification when a power setting changes.


## -parameters




### -param SettingGuid [in]

A GUID that represents the power setting.


### -param Flags [in]

Information about the recipient of the notification. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_SERVICE_HANDLE"></a><a id="device_notify_service_handle"></a><dl>
<dt><b>DEVICE_NOTIFY_SERVICE_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>Recipient</i> parameter is a handle to a service.Use the <a href="https://msdn.microsoft.com/47288924-3294-4a50-b27d-7df80d5c957c">CreateService</a> or <a href="https://msdn.microsoft.com/e0a42613-95ad-4d0f-a464-c6df33014064">OpenService</a> function to obtain this handle.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_NOTIFY_CALLBACK"></a><a id="device_notify_callback"></a><dl>
<dt><b>DEVICE_NOTIFY_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The <i>Recipient</i> parameter is a pointer to a callback function to call when the power setting changes.

</td>
</tr>
</table>
 


### -param Recipient [in]

A handle to the recipient of the notifications.


### -param RegistrationHandle [out]

A handle to the registration. Use this handle to unregister for notifications.


## -returns



Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed. 




## -remarks



Immediately after registration, the callback will be invoked with the current value of the power setting. If the registration occurs while the power setting is changing, you may receive multiple callbacks; the last callback is the most recent update. 




## -see-also




<a href="https://msdn.microsoft.com/39D432A7-54F8-4135-B98C-7290F95B054A">Power Setting GUIDs</a>



<a href="https://msdn.microsoft.com/9853c347-4528-43bb-8326-13bcd819b8a6">PowerSettingUnregisterNotification</a>
 

 

