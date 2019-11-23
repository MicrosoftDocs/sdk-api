---
UID: NF:msinkaut.IInkCustomStrokes.Remove
title: IInkCustomStrokes::Remove (msinkaut.h)

description: Removes the InkStrokes collection from the IInkCustomStrokes collection.
old-location: tablet\iinkcustromstrokes_remove.htm
tech.root: tablet
ms.assetid: 11cd07f2-0f02-42d6-8bab-b95456ed1926

ms.date: 12/05/2018
ms.keywords: 11cd07f2-0f02-42d6-8bab-b95456ed1926, IInkCustomStrokes interface [Tablet PC],Remove method, IInkCustomStrokes.Remove, IInkCustomStrokes::Remove, Remove, Remove method [Tablet PC], Remove method [Tablet PC],IInkCustomStrokes interface, msinkaut/IInkCustomStrokes::Remove, tablet.iinkcustromstrokes_remove
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkCustomStrokes.Remove"
dev_langs:
 - c++
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
 - IInkCustomStrokes.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCustomStrokes::Remove


## -description



Removes the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection from the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collection.




## -parameters




### -param Identifier [in]

The name or index of the collection of strokes to remove from the collection of custom strokes.

For more information about the VARIANT structure, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.


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
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid input parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_MISMATCHED_INK_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object don't match.

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
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
An invalid variant was passed in.

</td>
</tr>
</table>
 




## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes</a> collections are sets of references to ink data and are not the actual data itself. This method removes only the collection of strokes from a snapshot of, or reference to, the data and does not remove the actual ink data. To delete the collection from the actual ink data, call the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes</a> method of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

The <i>Identifier</i> parameter can be either a BSTR or a LONG. Use a BSTR for the name originally given to the custom stroke when it was added to the collection, and use a long for the index of the custom stroke in the collection. To specify the name of the custom stroke when you are using late binding, such as when you use a scripting language, you must pass in the argument as a string literal and not use a variable.

For more information about the BSTR data type, see <a href="https://docs.microsoft.com/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes">DeleteStrokes Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes">IInkCustomStrokes Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
 

 

