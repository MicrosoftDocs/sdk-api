---
UID: NF:msinkaut.IInkCursorButtons.Item
title: IInkCursorButtons::Item (msinkaut.h)
description: Retrieves the IInkCursorButton object at the specified index or string identifier within the IInkCursorButtons collection.
helpviewer_keywords: ["801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf","IInkCursorButtons interface [Tablet PC]","Item method","IInkCursorButtons.Item","IInkCursorButtons::Item","Item","Item method [Tablet PC]","Item method [Tablet PC]","IInkCursorButtons interface","msinkaut/IInkCursorButtons::Item","tablet.iinkcursorbuttons_item"]
old-location: tablet\iinkcursorbuttons_item.htm
tech.root: tablet
ms.assetid: 801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf
ms.date: 12/05/2018
ms.keywords: 801cc3f5-3e30-48b9-bf1b-8dbfaff08dbf, IInkCursorButtons interface [Tablet PC],Item method, IInkCursorButtons.Item, IInkCursorButtons::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkCursorButtons interface, msinkaut/IInkCursorButtons::Item, tablet.iinkcursorbuttons_item
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkCursorButtons::Item
 - msinkaut/IInkCursorButtons::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCursorButtons.Item
---

# IInkCursorButtons::Item


## -description

Retrieves the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> object at the specified index or string identifier within the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbuttons">IInkCursorButtons</a> collection.

## -parameters

### -param Identifier [in]

The zero-based index or BSTR identifier of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> object to get.

For more information about the VARIANT and BSTR data types, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param Button [out, retval]

Upon return, contains the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> object at the specified index within the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbuttons">IInkCursorButtons</a> collection.

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

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbuttons">IInkCursorButtons Interface</a>