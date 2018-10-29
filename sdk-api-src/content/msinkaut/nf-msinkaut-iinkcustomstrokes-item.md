---
UID: NF:msinkaut.IInkCustomStrokes.Item
title: IInkCustomStrokes::Item
author: windows-sdk-content
description: Retrieves the InkStrokes Collection at the location specified within the IInkCustomStrokes Interface.
old-location: tablet\iinkcustomstrokes_item.htm
tech.root: tablet
ms.assetid: 14cdc466-2acf-4af0-8fbc-74233edf3884
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 14cdc466-2acf-4af0-8fbc-74233edf3884, IInkCustomStrokes interface [Tablet PC],Item method, IInkCustomStrokes.Item, IInkCustomStrokes::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkCustomStrokes interface, msinkaut/IInkCustomStrokes::Item, tablet.iinkcustomstrokes_item
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCustomStrokes.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkCustomStrokes::Item


## -description



Retrieves the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a> at the location specified within the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes Interface</a>.




## -parameters




### -param Identifier [in]

The numeric index or string name of the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a> to return from the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes</a> collection.
          


### -param Strokes [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a> at the location specified within the <a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes Interface</a>.
          


## -returns



This method can return one of these values.

<table>
<tr>
<th>HRESULT Value</th>
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
Type OBJECT not registered.

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



An error occurs if the identifier doesn't match any existing member of the collection.

This method takes an input argument of type <b>VARIANT</b>. The subtype of this variable must be <b>BSTR</b> or <b>Long</b>.




## -see-also




<a href="https://msdn.microsoft.com/0b4eb5d6-ccf0-46c1-ae02-a393e67b817e">IInkCustomStrokes Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>



<a href="https://msdn.microsoft.com/ecffbdf0-4b1c-46de-bc4c-c44812dae27a">Item Method [InkStrokes Collection]</a>
 

 

