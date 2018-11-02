---
UID: NF:objidl.ISynchronizeContainer.AddSynchronize
title: ISynchronizeContainer::AddSynchronize
author: windows-sdk-content
description: Adds a synchronization object to the container.
old-location: com\isynchronizecontainer_addsynchronize.htm
tech.root: com
ms.assetid: b2d48de3-848c-4cc9-bd96-fffbb2ca2ba3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AddSynchronize, AddSynchronize method [COM], AddSynchronize method [COM],ISynchronizeContainer interface, ISynchronizeContainer interface [COM],AddSynchronize method, ISynchronizeContainer.AddSynchronize, ISynchronizeContainer::AddSynchronize, _com_isynchronizecontainer_addsynchronize, com.isynchronizecontainer_addsynchronize, objidlbase/ISynchronizeContainer::AddSynchronize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeContainer.AddSynchronize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISynchronizeContainer::AddSynchronize


## -description


Adds a synchronization object to the container.


## -parameters




### -param pSync [in]

A pointer to the synchronization object to be added to the container. See <a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_OUT_OF_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The synchronization object container is full.

</td>
</tr>
</table>
 




## -remarks



A synchronization container can hold pointers to as many as 63 synchronization objects.




## -see-also




<a href="https://msdn.microsoft.com/2c1e3d27-abb4-4bd0-ad9e-4dc9eda8e4b6">ISynchronize</a>



<a href="https://msdn.microsoft.com/6a5be504-b5fa-491c-ba65-74c5de39e263">ISynchronizeContainer</a>
 

 

