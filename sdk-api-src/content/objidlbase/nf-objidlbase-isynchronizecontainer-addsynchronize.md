---
UID: NF:objidlbase.ISynchronizeContainer.AddSynchronize
title: ISynchronizeContainer::AddSynchronize (objidlbase.h)
description: The ISynchronizeContainer::AddSynchronize (objidlbase.h) method adds a synchronization object to the container.
helpviewer_keywords: ["AddSynchronize","AddSynchronize method [COM]","AddSynchronize method [COM]","ISynchronizeContainer interface","ISynchronizeContainer interface [COM]","AddSynchronize method","ISynchronizeContainer.AddSynchronize","ISynchronizeContainer::AddSynchronize","_com_isynchronizecontainer_addsynchronize","com.isynchronizecontainer_addsynchronize","objidlbase/ISynchronizeContainer::AddSynchronize"]
old-location: com\isynchronizecontainer_addsynchronize.htm
tech.root: com
ms.assetid: b2d48de3-848c-4cc9-bd96-fffbb2ca2ba3
ms.date: 08/15/2022
ms.keywords: AddSynchronize, AddSynchronize method [COM], AddSynchronize method [COM],ISynchronizeContainer interface, ISynchronizeContainer interface [COM],AddSynchronize method, ISynchronizeContainer.AddSynchronize, ISynchronizeContainer::AddSynchronize, _com_isynchronizecontainer_addsynchronize, com.isynchronizecontainer_addsynchronize, objidlbase/ISynchronizeContainer::AddSynchronize
req.header: objidlbase.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISynchronizeContainer::AddSynchronize
 - objidlbase/ISynchronizeContainer::AddSynchronize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeContainer.AddSynchronize
---

# ISynchronizeContainer::AddSynchronize


## -description

Adds a synchronization object to the container.

## -parameters

### -param pSync [in]

A pointer to the synchronization object to be added to the container. See <a href="/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a>.

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

<a href="/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizecontainer">ISynchronizeContainer</a>
