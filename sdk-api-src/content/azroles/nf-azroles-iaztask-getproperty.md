---
UID: NF:azroles.IAzTask.GetProperty
title: IAzTask::GetProperty (azroles.h)
description: Returns the IAzTask object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_DATA","AZ_PROP_CHILD_CREATE","AZ_PROP_DESCRIPTION","AZ_PROP_NAME","AZ_PROP_TASK_BIZRULE","AZ_PROP_TASK_BIZRULE_LANGUAGE","AZ_PROP_TASK_IS_ROLE_DEFINITION","AZ_PROP_TASK_OPERATIONS","AZ_PROP_TASK_TASKS","AZ_PROP_WRITABLE","AzTask object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzTask object","GetProperty method [Security]","IAzTask interface","IAzTask interface [Security]","GetProperty method","IAzTask.GetProperty","IAzTask::GetProperty","azroles/IAzTask::GetProperty","security.iaztask_getproperty"]
old-location: security\iaztask_getproperty.htm
tech.root: security
ms.assetid: d484f56c-3d96-48df-a0d1-1bea58e30f26
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_DATA, AZ_PROP_CHILD_CREATE, AZ_PROP_DESCRIPTION, AZ_PROP_NAME, AZ_PROP_TASK_BIZRULE, AZ_PROP_TASK_BIZRULE_LANGUAGE, AZ_PROP_TASK_IS_ROLE_DEFINITION, AZ_PROP_TASK_OPERATIONS, AZ_PROP_TASK_TASKS, AZ_PROP_WRITABLE, AzTask object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzTask object, GetProperty method [Security],IAzTask interface, IAzTask interface [Security],GetProperty method, IAzTask.GetProperty, IAzTask::GetProperty, azroles/IAzTask::GetProperty, security.iaztask_getproperty
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzTask::GetProperty
 - azroles/IAzTask::GetProperty
dev_langs:
 - c++
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
---

# IAzTask::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object property  to return. The following table shows the possible values.

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
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_applicationdata">ApplicationData</a>  property

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
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_description">Description</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_name">Name</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE"></a><a id="az_prop_task_bizrule"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrule">BizRule</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_BIZRULE_LANGUAGE"></a><a id="az_prop_task_bizrule_language"></a><dl>
<dt><b>AZ_PROP_TASK_BIZRULE_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_bizrulelanguage">BizRuleLanguage</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_IS_ROLE_DEFINITION"></a><a id="az_prop_task_is_role_definition"></a><dl>
<dt><b>AZ_PROP_TASK_IS_ROLE_DEFINITION</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_isroledefinition">IsRoleDefinition</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_OPERATIONS"></a><a id="az_prop_task_operations"></a><dl>
<dt><b>AZ_PROP_TASK_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_operations">Operations</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_TASKS"></a><a id="az_prop_task_tasks"></a><dl>
<dt><b>AZ_PROP_TASK_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_tasks">Tasks</a>  property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also  accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-get_writable">Writable</a>  property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object property.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.