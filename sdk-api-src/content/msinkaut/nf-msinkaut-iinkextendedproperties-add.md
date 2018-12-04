---
UID: NF:msinkaut.IInkExtendedProperties.Add
title: IInkExtendedProperties::Add
author: windows-sdk-content
description: Creates and adds an IInkExtendedProperty object to the IInkExtendedProperties collection.
old-location: tablet\iinkextendedproperties_add.htm
tech.root: tablet
ms.assetid: 4fff6945-b46e-4e72-af45-ca066e73338e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 4fff6945-b46e-4e72-af45-ca066e73338e, Add, Add method [Tablet PC], Add method [Tablet PC],IInkExtendedProperties interface, IInkExtendedProperties interface [Tablet PC],Add method, IInkExtendedProperties.Add, IInkExtendedProperties::Add, msinkaut/IInkExtendedProperties::Add, tablet.iinkextendedproperties_add
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
 - IInkExtendedProperties.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkExtendedProperties::Add


## -description



Creates and adds an <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object to the <a href="https://msdn.microsoft.com/c7b7f40f-0c28-4848-83d6-d5db73eef998">IInkExtendedProperties</a> collection.




## -parameters




### -param Guid [in]

 The name of the new <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object. The name is expressed as a BSTR that represents the globally unique identifier (GUID) in the following format:

{dfc71f44-354b-4ca1-93d7-7459410b6343} (Including curly braces)

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param Data [in]

 The data for the new <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param InkExtendedProperty [out, retval]

When this method returns, contains a poitner to the new extended property.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The user did not specify data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

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
<dt><b>TPC_E_INVALID_STROKE</b></dt>
</dl>
</td>
<td width="60%">
The stroke is invalid.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  You cannot store an empty <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object. The object must contain data before it can be stored. For example, if you try to add extended properties to a stroke for later use, an exception is thrown if the extended property contains no data.</div>
<div> </div>
The following types are acceptable:

<ul>
<li>Byte or CHAR array</li>
<li>Arrays of integers, floats, large integers, doubles, dates, or decimals</li>
<li>Booleans (but not arrays of Booleans)</li>
<li>BSTRs (but not arrays of BSTRs)</li>
<li>Arrays of Variants. All arrays of variants passed as an <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> must be of the same type and be all numeric. For example, variant arrays of BSTRS, arrays of arrays, VT_NULL and VT_EMPTY are not supported.</li>
</ul>
<div class="alert"><b>Note</b>  If you call this method with the <i>Guid</i> parameter set to a GUID that already exists in the <a href="https://msdn.microsoft.com/c7b7f40f-0c28-4848-83d6-d5db73eef998">IInkExtendedProperties</a> collection, the new data will replace the existing extended property for that GUID instead of adding a second element.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c7b7f40f-0c28-4848-83d6-d5db73eef998">IInkExtendedProperties Interface</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

