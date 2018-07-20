---
UID: NF:tapi3if.ITCollection2.Remove
title: ITCollection2::Remove
author: windows-sdk-content
description: The Remove method deletes an item from the collection at the specified index.
old-location: tapi3\itcollection2_remove.htm
old-project: tapi
ms.assetid: 27e46c36-8704-4e33-ad2a-5888d701651c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITCollection2 interface [TAPI 2.2],Remove method, ITCollection2.Remove, ITCollection2::Remove, Remove, Remove method [TAPI 2.2], Remove method [TAPI 2.2],ITCollection2 interface, _tapi3_itcollection2_remove, tapi3.itcollection2_remove, tapi3if/ITCollection2::Remove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCollection2.Remove
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCollection2::Remove


## -description


The 
<b>Remove</b> method deletes an item from the collection at the specified index.


## -parameters




### -param Index [in]

Specifies the location in the collection of the item to remove.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Index</i> parameter does not specify a valid index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to reallocate the collection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>



<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a>
 

 

