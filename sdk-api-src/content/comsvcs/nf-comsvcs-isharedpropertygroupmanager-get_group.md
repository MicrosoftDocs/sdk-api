---
UID: NF:comsvcs.ISharedPropertyGroupManager.get_Group
title: ISharedPropertyGroupManager::get_Group
author: windows-sdk-content
description: Retrieves a reference to an existing shared property group.
old-location: cos\isharedpropertygroupmanager_get_group.htm
old-project: cossdk
ms.assetid: 3e60d1c6-1d58-403a-b75f-2a6bea91081e
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ISharedPropertyGroupManager interface [COM+],get_Group method, ISharedPropertyGroupManager.get_Group, ISharedPropertyGroupManager::get_Group, _cos_ISharedPropertyGroupManager_get_Group, comsvcs/ISharedPropertyGroupManager::get_Group, cos.isharedpropertygroupmanager_get_group, get_Group, get_Group method [COM+], get_Group method [COM+],ISharedPropertyGroupManager interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedPropertyGroupManager.get_Group
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISharedPropertyGroupManager::get_Group


## -description


Retrieves a reference to an existing shared property group.


## -parameters




### -param Name [in]

The name of the shared property group to be retrieved.


### -param ppGroup [out]

A reference to the shared property group specified in the <i>Name</i> parameter, or <b>NULL</b> if the property group does not exist. 


## -returns



This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The shared property group exists, and a reference to it is returned in the <i>ppGroup</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The shared property group with the name specified in the <i>Name</i> parameter does not exist.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/71c0a1de-5ea5-4496-b0e9-56d0cc8129a9">ISharedPropertyGroupManager</a>
 

 

