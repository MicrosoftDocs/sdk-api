---
UID: NF:msinkaut.IInkDisp.Clone
title: IInkDisp::Clone (msinkaut.h)
description: Creates a duplicate InkDisp object.helpviewer_keywords: ["Clone","Clone method [Tablet PC]","Clone method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","Clone method","IInkDisp.Clone","IInkDisp::Clone","f3ec6b42-2b5d-459e-ba09-88c27b125c40","msinkaut/IInkDisp::Clone","tablet.inkdisp_clone"]
old-location: tablet\inkdisp_clone.htm
tech.root: tablet
ms.assetid: f3ec6b42-2b5d-459e-ba09-88c27b125c40
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Tablet PC], Clone method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],Clone method, IInkDisp.Clone, IInkDisp::Clone, f3ec6b42-2b5d-459e-ba09-88c27b125c40, msinkaut/IInkDisp::Clone, tablet.inkdisp_clone
f1_keywords:
- msinkaut/IInkDisp.Clone
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
- IInkDisp.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDisp::Clone


## -description



Creates a duplicate <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.




## -parameters




### -param NewInk [out, retval]

When this method returns, contains a pointer to the newly created <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.


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
<dt><b>REGDB_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object was not registered.

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
</table>
 




## -remarks



The <b>Clone</b> method is defined for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a>, and <a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> objects. The <b>Clone</b> method returns an exact copy of the original object.

In most scenarios, the duplicate object is an exact copy of the original object, but no relation between the two objects exists. See the remarks section of this topic for details on exceptions to this.


<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> object: The only scenario in which the duplicate <b>InkDisp</b> object is not an exact copy of the original object is when a dirty <b>InkDisp</b> object is cloned. In this case, the duplicate <b>InkDisp</b> object's <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty">Dirty</a> property is <b>FALSE</b>. All other properties of the cloned <b>InkDisp</b> object are exact copies.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty">Dirty Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846797(v=VS.85).aspx">IInkDisp</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes Method</a>
 

 

