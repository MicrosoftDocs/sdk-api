---
UID: NF:wuapi.IUpdateCollection.RemoveAt
title: IUpdateCollection::RemoveAt
author: windows-sdk-content
description: Removes the item at the specified index from the collection.
old-location: wua\iupdatecollection_removeat.htm
old-project: Wua_Sdk
ms.assetid: b6d32db8-c935-41f8-a8f3-0730719cac7e
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IUpdateCollection interface [Windows Update Agent],RemoveAt method, IUpdateCollection.RemoveAt, IUpdateCollection::RemoveAt, RemoveAt, RemoveAt method [Windows Update Agent], RemoveAt method [Windows Update Agent],IUpdateCollection interface, wua.iupdatecollection_removeat, wuapi/IUpdateCollection::RemoveAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateCollection::RemoveAt


## -description


Removes the item at the specified index from the collection.


## -parameters




### -param index [in]

The index of the interface to be removed.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
An index is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e56a09e9-6a5f-4579-9a5c-987519fccaad">IUpdateCollection</a>
 

 

