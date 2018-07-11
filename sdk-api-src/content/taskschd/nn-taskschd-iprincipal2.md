---
UID: NN:taskschd.IPrincipal2
title: IPrincipal2
author: windows-sdk-content
description: Provides the extended settings applied to security credentials for a principal.
old-location: taskschd\iprincipal2.htm
old-project: taskschd
ms.assetid: 480f8038-0f67-4a69-b6f6-d7ba881d9d57
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IPrincipal2, IPrincipal2 interface [Task Scheduler], IPrincipal2 interface [Task Scheduler],described, taskschd.iprincipal2, taskschd/IPrincipal2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IPrincipal2
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IPrincipal2 interface


## -description


Provides the extended settings applied to security credentials  for a principal. These security credentials define the security context for the tasks that are associated with the principal.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrincipal2</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IPrincipal2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IPrincipal2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b7fffa-7e16-43e1-9176-677d9948f448">AddRequiredPrivilege</a>
</td>
<td align="left" width="63%">
Adds a privilege to the to the task process token.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrincipal2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/73bd517f-5496-482e-ad9d-59066689e84a">ProcessTokenSidType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the process token security identifier (SID) type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/701ff07e-2dd1-4985-8fc4-f570749c5834">RequiredPrivilege</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the required privilege by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b80cb1ad-8d28-4e38-82c4-92f1ce8fbc55">RequiredPrivilegeCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of privileges in the required privileges array.

</td>
</tr>
</table> 


## -remarks



When reading or writing XML for a task, the security credentials for a principal are specified in the <a href="https://msdn.microsoft.com/4ba65976-98d2-4329-80f0-566fac2e9fda">Principal</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a> or <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a>



<a href="https://msdn.microsoft.com/d1c8389b-149c-4fcb-972a-b25fa0d8d763">Principal Property of ITaskDefinition</a>



<a href="https://msdn.microsoft.com/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

