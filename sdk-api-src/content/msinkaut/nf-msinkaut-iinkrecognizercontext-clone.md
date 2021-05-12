---
UID: NF:msinkaut.IInkRecognizerContext.Clone
title: IInkRecognizerContext::Clone (msinkaut.h)
description: Creates a duplicate InkRecognizerContext object.
helpviewer_keywords: ["Clone","Clone method [Tablet PC]","Clone method [Tablet PC]","IInkRecognizerContext interface","IInkRecognizerContext interface [Tablet PC]","Clone method","IInkRecognizerContext.Clone","IInkRecognizerContext::Clone","f3ec6b42-2b5d-459e-ba09-88c27b125c40","get_Clone","msinkaut/IInkRecognizerContext::Clone","putref_Clone","tablet.inkrecognizercontext_clone"]
old-location: tablet\inkrecognizercontext_clone.htm
tech.root: tablet
ms.assetid: f376e177-7714-4771-8aa4-13f91a26395a
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Tablet PC], Clone method [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],Clone method, IInkRecognizerContext.Clone, IInkRecognizerContext::Clone, f3ec6b42-2b5d-459e-ba09-88c27b125c40, get_Clone, msinkaut/IInkRecognizerContext::Clone, putref_Clone, tablet.inkrecognizercontext_clone
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
 - IInkRecognizerContext::Clone
 - msinkaut/IInkRecognizerContext::Clone
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
 - IInkRecognizerContext.Clone
---

# IInkRecognizerContext::Clone


## -description

Creates a duplicate <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

## -parameters

### -param RecoContext [out, retval]

When this method returns, contains the newly created <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object.

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
The <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object was not registered.

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

The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone">Clone</a> method is defined for the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a>, <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a>, and <a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> objects. The <b>Clone</b> method returns an exact copy of the original object.

In most scenarios, the duplicate object is an exact copy of the original object, but no relation between the two objects exists. See the remarks section of this topic for details on exceptions to this.


<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext</a> object: This method returns a copy of the original <b>InkRecognizerContext</b> that contains the same settings as the original, but does not include the recognition results, if any. The settings that are copied include the recognition guide, character Autocomplete mode, a reference to the original <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a>, and all properties that improve the recognition results, such as the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid">Factoid</a> property and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags</a> property.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty">Dirty Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes">ModifyDrawingAttributes Method</a>
