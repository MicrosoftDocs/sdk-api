---
UID: NF:msinkaut.IInkCursorButtons.Item
title: IInkCursorButtons::Item
author: windows-driver-content
description: Retrieves the IInkCursorButton object at the specified index or string identifier within the IInkCursorButtons collection.
old-location: tablet\iinkcursorbuttons_item.htm
old-project: tablet
ms.assetid: 801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf, IInkCursorButtons interface [Tablet PC],Item method, IInkCursorButtons.Item, IInkCursorButtons::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkCursorButtons interface, msinkaut/IInkCursorButtons::Item, tablet.iinkcursorbuttons_item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkCursorButtons.Item
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkCursorButtons::Item


## -description



Retrieves the <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> object at the specified index or string identifier within the <a href="https://msdn.microsoft.com/3f695ab4-8174-402f-b7d6-810f149f5153">IInkCursorButtons</a> collection.




## -parameters




### -param Identifier




### -param Button [out, retval]

Upon return, contains the <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> object at the specified index within the <a href="https://msdn.microsoft.com/3f695ab4-8174-402f-b7d6-810f149f5153">IInkCursorButtons</a> collection.


#### - identifier [in]

The zero-based index or BSTR identifier of the <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> object to get.

For more information about the VARIANT and BSTR data types, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not a valid VARIANT type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
Type object not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

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
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_RECOGNIZER_NOT_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The recognizers registry key is corrupted or your environment does not support handwriting recognition.

</td>
</tr>
</table>
 




## -remarks



An error occurs if the index doesn't match any existing member of the collection.

The <b>Item</b> method takes an input argument of type VARIANT. However, the subtype of this variable must be integer or string (BSTR). This means that when you are using late binding, such as when you use a scripting language, you must pass in the argument as a STRING literal and not use a variable.




## -see-also




<a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton Interface</a>



<a href="https://msdn.microsoft.com/3f695ab4-8174-402f-b7d6-810f149f5153">IInkCursorButtons Interface</a>
 

 

