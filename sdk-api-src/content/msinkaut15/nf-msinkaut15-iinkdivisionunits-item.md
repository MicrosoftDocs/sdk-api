---
UID: NF:msinkaut15.IInkDivisionUnits.Item
title: IInkDivisionUnits::Item
author: windows-sdk-content
description: Retrieves the IInkDivisionUnit object at the specified index within the IInkDivisionUnits collection.
old-location: tablet\iinkdivisionunits_item.htm
tech.root: tablet
ms.assetid: 332a9365-526e-43df-841f-20eed07762e7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 332a9365-526e-43df-841f-20eed07762e7, IInkDivisionUnits interface [Tablet PC],Item method, IInkDivisionUnits.Item, IInkDivisionUnits::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkDivisionUnits interface, msinkaut15/IInkDivisionUnits::Item, tablet.iinkdivisionunits_item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut15.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Inkdiv.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Inkdiv.dll
 - Inkdiv.dll.dll
api_name:
 - IInkDivisionUnits.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDivisionUnits::Item


## -description



Retrieves the <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object at the specified index within the <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection.




## -parameters




### -param Index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object to get.


### -param InkDivisionUnit [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit</a> object at the specified index within the <a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits</a> collection.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



An error occurs if the index doesn't match any existing member of the collection.




## -see-also




<a href="https://msdn.microsoft.com/5c5479e0-7568-40c8-bb75-e2ded3ac86b7">IInkDivisionUnit Interface</a>



<a href="https://msdn.microsoft.com/efce8756-f42b-4d9a-bfed-4297e7e0fdec">IInkDivisionUnits Interface</a>
 

 

