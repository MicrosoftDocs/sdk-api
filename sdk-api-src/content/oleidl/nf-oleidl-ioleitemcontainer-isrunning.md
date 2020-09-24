---
UID: NF:oleidl.IOleItemContainer.IsRunning
title: IOleItemContainer::IsRunning (oleidl.h)
description: Determines whether the specified object is running.
helpviewer_keywords: ["IOleItemContainer interface [COM]","IsRunning method","IOleItemContainer.IsRunning","IOleItemContainer::IsRunning","IsRunning","IsRunning method [COM]","IsRunning method [COM]","IOleItemContainer interface","_com_ioleitemcontainer_isrunning","com.ioleitemcontainer_isrunning","oleidl/IOleItemContainer::IsRunning"]
old-location: com\ioleitemcontainer_isrunning.htm
tech.root: com
ms.assetid: 7bbd7b58-b7ab-493e-8315-a35034ee2b7a
ms.date: 12/05/2018
ms.keywords: IOleItemContainer interface [COM],IsRunning method, IOleItemContainer.IsRunning, IOleItemContainer::IsRunning, IsRunning, IsRunning method [COM], IsRunning method [COM],IOleItemContainer interface, _com_ioleitemcontainer_isrunning, com.ioleitemcontainer_isrunning, oleidl/IOleItemContainer::IsRunning
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.idl
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
 - IOleItemContainer::IsRunning
 - oleidl/IOleItemContainer::IsRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleItemContainer.IsRunning
---

# IOleItemContainer::IsRunning


## -description

Determines whether the specified object is running.

## -parameters

### -param pszItem [in]

The container's name for the object.

## -returns

This method can return the following values.

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
The object is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The parameter does not identify an object in this container.

</td>
</tr>
</table>

## -remarks

The item moniker implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-isrunning">IMoniker::IsRunning</a> calls this method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of <b>IOleItemContainer::IsRunning</b> should first determine whether <i>pszItem</i> identifies one of the container's objects. If it does not, your implementation should return MK_E_NOOBJECT. If the object is not loaded, your implementation should return S_FALSE. If it is loaded, your implementation can call the <a href="/windows/desktop/api/ole2/nf-ole2-oleisrunning">OleIsRunning</a> function to determine whether it is running.

If <i>pszItem</i> names a pseudo-object, your implementation can simply return S_OK because a pseudo-object is running whenever its container is running.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>