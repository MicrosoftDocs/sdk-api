---
UID: NN:taskschd.IRegisteredTask
title: IRegisteredTask
author: windows-sdk-content
description: Provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.
old-location: taskschd\iregisteredtask.htm
tech.root: TaskSchd
ms.assetid: 3743d012-ad7c-402f-8859-939bb01ee447
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRegisteredTask, IRegisteredTask interface [Task Scheduler], IRegisteredTask interface [Task Scheduler],described, taskschd.iregisteredtask, taskschd/IRegisteredTask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRegisteredTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegisteredTask interface


## -description


Provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the  properties that describe the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredTask</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRegisteredTask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRegisteredTask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4634851e-e868-4915-a7da-32a39f405974">GetInstances</a>
</td>
<td align="left" width="63%">
Returns all instances of the registered task that are currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ab41687-085a-414d-8054-9c6fe7439e4e">GetRunTimes</a>
</td>
<td align="left" width="63%">
Gets the times that the registered task is scheduled to run during a specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/474d62a5-9ec7-40f7-b26e-54923f8ebe1e">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor that is used as credentials for the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b237ddd-e4e8-47f7-97e7-360e79841acc">Run</a>
</td>
<td align="left" width="63%">
Runs the registered task immediately.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6d09ab1-026d-4ee9-b520-c7702e37504e">RunEx</a>
</td>
<td align="left" width="63%">
Runs the registered task immediately using specified flags and a session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c8ebfdb-3c23-4fec-9023-7a944d99a409">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor that is used as credentials for the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c58d7b15-1044-4d35-a501-b936503ee0fc">Stop</a>
</td>
<td align="left" width="63%">
Stops the registered task immediately.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredTask</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/673d5e11-d2a3-4dcb-ad2e-46940574ba92">Definition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the definition of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/33486621-3984-4a07-8182-c193847a9f76">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a Boolean value that indicates if the registered task is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c7ac7fea-35c7-4336-9142-6c97caa1dea0">LastRunTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the time the registered task was last run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a16b0b01-109b-44ae-8318-dbc5d6728e17">LastTaskResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the results that were returned the last time the registered task was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17aff717-10dd-43ac-9d14-6c07831d4c18">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ccaed6d7-4247-4299-9226-77d84d572e3b">NextRunTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the time when the registered task is next scheduled to run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8f5b5471-edfa-45e6-b556-ba12c0721aed">NumberOfMissedRuns</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of times the registered task has missed a scheduled run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf097dae-d92b-48c8-bc96-8169b94b0763">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the path to where the registered task is stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b5ac2207-b5c0-42bd-a059-93a2c1f49f33">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the operational state of the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cfa85a88-99f5-4c4f-afe8-44b3f27833e5">XML</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the XML-formatted registration information for the registered task.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

