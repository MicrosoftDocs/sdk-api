---
UID: NF:msinkaut.IInkTablets.Item
title: IInkTablets::Item
author: windows-sdk-content
description: Retrieves the IInkTablet object at the specified index within the InkTablets collection.
old-location: tablet\inktablets_item.htm
tech.root: tablet
ms.assetid: 02ead8bd-9f96-4862-b9b4-b1f3def1efa6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: 02ead8bd-9f96-4862-b9b4-b1f3def1efa6, IInkTablets interface [Tablet PC],Item method, IInkTablets.Item, IInkTablets::Item, Item, Item method [Tablet PC], Item method [Tablet PC],IInkTablets interface, msinkaut/IInkTablets::Item, tablet.inktablets_item
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
 - IInkTablets.Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkTablets::Item


## -description



Retrieves the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object at the specified index within the <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection.




## -parameters




### -param Index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object to get.


### -param Tablet [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object at the specified index within the <a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets</a> collection.


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

<div class="alert"><b>Note</b>  This function can be re-entered when called within certain message handlers, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/98052ECB-9385-45C9-A03C-3F312ADD9872">IInkTablets</a>



<a href="https://msdn.microsoft.com/ef1cb6dc-d656-4b30-9c7d-e482cef6b9ae">InkTablets Collection</a>
 

 

