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

# PowerClearRequest function


## -description


Decrements the count of power requests of the specified type for a power request object.


## -parameters




### -param PowerRequest [in]

A handle to a power request object.


### -param RequestType [in]

The power request type to be decremented. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PowerRequestDisplayRequired"></a><a id="powerrequestdisplayrequired"></a><a id="POWERREQUESTDISPLAYREQUIRED"></a><dl>
<dt><b>PowerRequestDisplayRequired</b></dt>
</dl>
</td>
<td width="60%">
The display remains on even if there is no user input for an extended period of time.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestSystemRequired"></a><a id="powerrequestsystemrequired"></a><a id="POWERREQUESTSYSTEMREQUIRED"></a><dl>
<dt><b>PowerRequestSystemRequired</b></dt>
</dl>
</td>
<td width="60%">
The system continues to run instead of entering sleep after a period of user inactivity.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestAwayModeRequired"></a><a id="powerrequestawaymoderequired"></a><a id="POWERREQUESTAWAYMODEREQUIRED"></a><dl>
<dt><b>PowerRequestAwayModeRequired</b></dt>
</dl>
</td>
<td width="60%">
The system enters away mode instead of sleep. In away mode, the system continues to run but turns off audio and video to give the appearance of sleep.

</td>
</tr>
<tr>
<td width="40%"><a id="PowerRequestExecutionRequired"></a><a id="powerrequestexecutionrequired"></a><a id="POWERREQUESTEXECUTIONREQUIRED"></a><dl>
<dt><b>PowerRequestExecutionRequired</b></dt>
</dl>
</td>
<td width="60%">
The calling process continues to run instead of being suspended or terminated by process lifetime management mechanisms. When and how long the process is allowed to run depends on the operating system and  power policy settings. 

When a <b>PowerRequestExecutionRequired</b> request is active, it implies <b>PowerRequestSystemRequired</b>.

The <b>PowerRequestExecutionRequired</b> request type can be used only by applications. Services cannot use this request type.

<b>Windows 7 and Windows Server 2008 R2:  </b>This request type is supported starting with Windows 8 and Windows Server 2012.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2122bf00-9e6b-48ab-89b0-f53dd6804902">PowerCreateRequest</a>



<a href="https://msdn.microsoft.com/85249de8-5832-4f25-bbd9-3576cfd1caa0">PowerSetRequest</a>
 

 

