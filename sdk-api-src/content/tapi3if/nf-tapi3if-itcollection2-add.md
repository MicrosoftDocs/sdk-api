---
UID: NF:tapi3if.ITCollection2.Add
title: ITCollection2::Add method
author: windows-driver-content
description: The Add method inserts a new item into the collection at the specified index.
old-location: tapi3\itcollection2_add.htm
old-project: Tapi
ms.assetid: 96c26f76-3835-4140-8379-91171fc4ad37
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: Add method [TAPI 2.2], Add method [TAPI 2.2], ITCollection2 interface, Add,ITCollection2.Add, ITCollection2, ITCollection2 interface [TAPI 2.2], Add method, ITCollection2::Add, _tapi3_itcollection2_add, tapi3.itcollection2_add, tapi3if/ITCollection2::Add
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITCollection2.Add
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCollection2::Add method


## -description


The 
<b>Add</b> method inserts a new item into the collection at the specified index.


## -parameters




### -param Index [in]

Specifies the location in the collection where the item should be added.


### -param pVariant [in]

Pointer to a <b>VARIANT</b> containing the item to add.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

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




<a href="https://msdn.microsoft.com/d65f06c9-fecd-4ce6-af82-81acb48268e5">ITCollection2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
 

 

