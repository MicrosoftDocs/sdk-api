---
UID: NF:msinkaut.IInkDisp.CanPaste
title: IInkDisp::CanPaste (msinkaut.h)
description: Indicates whether the IDataObject can be converted to an InkDisp object.
helpviewer_keywords: ["755c74c4-417a-49b5-9f3d-9348c05ac850","CanPaste","CanPaste method [Tablet PC]","CanPaste method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","CanPaste method","IInkDisp.CanPaste","IInkDisp::CanPaste","msinkaut/IInkDisp::CanPaste","tablet.inkdisp_canpaste"]
old-location: tablet\inkdisp_canpaste.htm
tech.root: tablet
ms.assetid: 755c74c4-417a-49b5-9f3d-9348c05ac850
ms.date: 12/05/2018
ms.keywords: 755c74c4-417a-49b5-9f3d-9348c05ac850, CanPaste, CanPaste method [Tablet PC], CanPaste method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],CanPaste method, IInkDisp.CanPaste, IInkDisp::CanPaste, msinkaut/IInkDisp::CanPaste, tablet.inkdisp_canpaste
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
 - IInkDisp::CanPaste
 - msinkaut/IInkDisp::CanPaste
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
 - IInkDisp.CanPaste
---

# IInkDisp::CanPaste


## -description

Indicates whether the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> can be converted to an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -parameters

### -param DataObject [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> to inspect. The default value is <b>NULL</b>, which means the data object on the Clipboard is used.

### -param CanPaste [out, retval]

<b>VARIANT_TRUE</b> if the data object can be converted to an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object; otherwise, <b>VARIANT_FALSE</b>.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -remarks

If the supplied <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> is <b>NULL</b>, then the data object on the Clipboard is used.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
