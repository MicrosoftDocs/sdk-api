---
UID: NF:azroles.IAzTask.AddPropertyItem
title: IAzTask::AddPropertyItem
author: windows-driver-content
description: Adds the specified entity to the specified list.
old-location: security\iaztask_addpropertyitem.htm
old-project: SecAuthZ
ms.assetid: 50d8c1f2-11c3-41d8-b935-a8f296d2c18f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: AZ_PROP_TASK_OPERATIONS, AZ_PROP_TASK_TASKS, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzTask object, AddPropertyItem method [Security],IAzTask interface, AzTask object [Security],AddPropertyItem method, IAzTask interface [Security],AddPropertyItem method, IAzTask.AddPropertyItem, IAzTask::AddPropertyItem, azroles/IAzTask::AddPropertyItem, security.iaztask_addpropertyitem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzTask.AddPropertyItem
-	AzTask.AddPropertyItem
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
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
Can also be added using the <a href="https://msdn.microsoft.com/73da7094-440c-4e68-8d43-9f4ba26dd14b">AddOperation</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_TASK_TASKS"></a><a id="az_prop_task_tasks"></a><dl>
<dt><b>AZ_PROP_TASK_TASKS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/6b3057d1-26aa-443c-857f-0057ef9d2072">AddTask</a> method

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



You must call the <a href="https://msdn.microsoft.com/a6f01573-c1ee-421d-8591-e1c9fa6c3d68">Submit</a> method to persist any changes made by this method.



