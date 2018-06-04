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

# NetworkIsolationRegisterForAppContainerChanges function


## -description


The <b>NetworkIsolationRegisterForAppContainerChanges</b> function is used to register for the delivery of notifications regarding changes to an app container.


## -parameters




### -param flags [in]

Type: <b>DWORD</b>

A bitmask value of control flags which specify when to receive notifications. May contain one or more of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_NONE"></a><a id="inet_firewall_ac_none"></a><dl>
<dt><b>INET_FIREWALL_AC_NONE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
No notifications will be delivered.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_PACKAGE_ID_ONLY_"></a><a id="inet_firewall_ac_package_id_only_"></a><dl>
<dt><b>INET_FIREWALL_AC_PACKAGE_ID_ONLY </b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Notifications will be delivered when an app container is created with a package identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_BINARY"></a><a id="inet_firewall_ac_binary"></a><dl>
<dt><b>INET_FIREWALL_AC_BINARY</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Notifications will be delivered when  an app container is created with a binary path.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_MAX"></a><a id="inet_firewall_ac_max"></a><dl>
<dt><b>INET_FIREWALL_AC_MAX</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Maximum value for testing purposes.

</td>
</tr>
</table>
 


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/7a2afc36-c250-4eb1-9853-d79def85bb67">PAC_CHANGES_CALLBACK_FN</a></b>

Function pointer that will be invoked when a notification is ready for delivery.


### -param context [in, optional]

Type: <b>PVOID</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the change. 


### -param registrationObject [out]

Type: <b>HANDLE*</b>

Handle to the newly created registration.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise. 




## -see-also




<a href="https://msdn.microsoft.com/589f416d-058a-4711-863f-74b0dacc63eb">NetworkIsolationUnregisterForAppContainerChanges</a>



<a href="https://msdn.microsoft.com/7a2afc36-c250-4eb1-9853-d79def85bb67">PAC_CHANGES_CALLBACK_FN</a>
 

 

