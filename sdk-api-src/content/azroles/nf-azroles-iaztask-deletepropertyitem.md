---
UID: NF:azroles.IAzTask.DeletePropertyItem
title: IAzTask::DeletePropertyItem (azroles.h)
description: Removes the specified entity from the specified list. (IAzTask.DeletePropertyItem)
helpviewer_keywords: ["AZ_PROP_TASK_OPERATIONS","AZ_PROP_TASK_TASKS","AzTask object [Security]","DeletePropertyItem method","DeletePropertyItem","DeletePropertyItem method [Security]","DeletePropertyItem method [Security]","AzTask object","DeletePropertyItem method [Security]","IAzTask interface","IAzTask interface [Security]","DeletePropertyItem method","IAzTask.DeletePropertyItem","IAzTask::DeletePropertyItem","azroles/IAzTask::DeletePropertyItem","security.iaztask_deletepropertyitem"]
old-location: security\iaztask_deletepropertyitem.htm
tech.root: security
ms.assetid: 4a9ffd54-cd1c-46ab-ab22-5c999b60d802
ms.date: 12/05/2018
ms.keywords: AZ_PROP_TASK_OPERATIONS, AZ_PROP_TASK_TASKS, AzTask object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzTask object, DeletePropertyItem method [Security],IAzTask interface, IAzTask interface [Security],DeletePropertyItem method, IAzTask.DeletePropertyItem, IAzTask::DeletePropertyItem, azroles/IAzTask::DeletePropertyItem, security.iaztask_deletepropertyitem
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
 - IAzTask::DeletePropertyItem
 - azroles/IAzTask::DeletePropertyItem
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
 - IAzTask.DeletePropertyItem
 - AzTask.DeletePropertyItem
---

# IAzTask::DeletePropertyItem


## -description

The <b>DeletePropertyItem</b> method removes the specified entity from the specified list.

## -parameters

### -param lPropId [in]

Property ID of the  list from which to remove the entity specified by the <i>varProp</i> parameter. The following table shows the possible values.

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
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-deleteoperation">DeleteOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_TASKS"></a><a id="az_prop_task_tasks"></a><dl>
<dt><b>AZ_PROP_TASK_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-deletetask">DeleteTask</a> method

</td>
</tr>
</table>

### -param varProp [in]

Name of the entity to remove from the list  specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.
