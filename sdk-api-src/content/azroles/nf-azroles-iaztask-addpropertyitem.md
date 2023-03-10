---
UID: NF:azroles.IAzTask.AddPropertyItem
title: IAzTask::AddPropertyItem (azroles.h)
description: Adds the specified entity to the specified list. (IAzTask.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_TASK_OPERATIONS","AZ_PROP_TASK_TASKS","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzTask object","AddPropertyItem method [Security]","IAzTask interface","AzTask object [Security]","AddPropertyItem method","IAzTask interface [Security]","AddPropertyItem method","IAzTask.AddPropertyItem","IAzTask::AddPropertyItem","azroles/IAzTask::AddPropertyItem","security.iaztask_addpropertyitem"]
old-location: security\iaztask_addpropertyitem.htm
tech.root: security
ms.assetid: 50d8c1f2-11c3-41d8-b935-a8f296d2c18f
ms.date: 12/05/2018
ms.keywords: AZ_PROP_TASK_OPERATIONS, AZ_PROP_TASK_TASKS, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzTask object, AddPropertyItem method [Security],IAzTask interface, AzTask object [Security],AddPropertyItem method, IAzTask interface [Security],AddPropertyItem method, IAzTask.AddPropertyItem, IAzTask::AddPropertyItem, azroles/IAzTask::AddPropertyItem, security.iaztask_addpropertyitem
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
 - IAzTask::AddPropertyItem
 - azroles/IAzTask::AddPropertyItem
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
 - IAzTask.AddPropertyItem
 - AzTask.AddPropertyItem
---

# IAzTask::AddPropertyItem


## -description

The <b>AddPropertyItem</b> method adds the specified entity to the specified list.

## -parameters

### -param lPropId [in]

Property ID of the  list to which to add the entity specified by the <i>varProp</i> parameter. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_OPERATIONS"></a><a id="az_prop_task_operations"></a><dl>
<dt><b>AZ_PROP_TASK_OPERATIONS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-addoperation">AddOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_TASKS"></a><a id="az_prop_task_tasks"></a><dl>
<dt><b>AZ_PROP_TASK_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-addtask">AddTask</a> method

</td>
</tr>
</table>

### -param varProp [in]

Name of the entity to add to the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">Submit</a> method to persist any changes made by this method.
