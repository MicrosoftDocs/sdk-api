---
UID: NF:azroles.IAzTask.GetProperty
title: IAzTask::GetProperty
author: windows-sdk-content
description: Returns the IAzTask object property with the specified property ID.
old-location: security\iaztask_getproperty.htm
old-project: SecAuthZ
ms.assetid: d484f56c-3d96-48df-a0d1-1bea58e30f26
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_TASK_BIZRULE, AZ_PROP_TASK_BIZRULE_LANGUAGE, AZ_PROP_TASK_IS_ROLE_DEFINITION, AZ_PROP_TASK_OPERATIONS, AZ_PROP_TASK_TASKS, AZ_PROP_WRITABLE, AzTask object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzTask object, GetProperty method [Security],IAzTask interface, IAzTask interface [Security],GetProperty method, IAzTask.GetProperty, IAzTask::GetProperty, azroles/IAzTask::GetProperty, security.iaztask_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask.GetProperty
 - AzTask.GetProperty
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::GetProperty


## -description


The <b>GetProperty</b> method returns the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property  with the specified property ID.


## -parameters




### -param lPropId [in]

Property ID of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property  to return. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/0a3939ee-6449-4eef-bb23-11e6d7018f04">ApplicationData</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value is <b>TRUE</b> if the current user has permission; otherwise, <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE"></a><a id="az_prop_task_bizrule"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/cf3d87af-5320-4fe0-b513-e242f8a1dd1b">BizRule</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE_LANGUAGE"></a><a id="az_prop_task_bizrule_language"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/922f4fd8-f553-439c-b9ae-51a45a88adc7">BizRuleLanguage</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_IS_ROLE_DEFINITION"></a><a id="az_prop_task_is_role_definition"></a><dl>
<dt><b>AZ_PROP_TASK_IS_ROLE_DEFINITION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/fef32545-de7e-4516-a289-b9ddf45b7c81">IsRoleDefinition</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_OPERATIONS"></a><a id="az_prop_task_operations"></a><dl>
<dt><b>AZ_PROP_TASK_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/b05fd157-6526-49d6-9bb1-fcf8c59cc74e">Operations</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_TASKS"></a><a id="az_prop_task_tasks"></a><dl>
<dt><b>AZ_PROP_TASK_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/a4baa899-78eb-4a3b-bcc1-0b8c2831b10f">Tasks</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="https://msdn.microsoft.com/68f31203-00de-4729-a836-51d5dc8c8091">Writable</a>  property

</td>
</tr>
</table>
 


### -param varReserved [in, optional]

Reserved for future use.


### -param pvarProp [out]

A pointer to the returned <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object property.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



