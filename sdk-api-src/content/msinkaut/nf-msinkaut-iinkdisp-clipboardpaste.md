---
UID: NF:msinkaut.IInkDisp.ClipboardPaste
title: IInkDisp::ClipboardPaste (msinkaut.h)
description: Copies the IDataObject from the Clipboard to the InkDisp object.
helpviewer_keywords: ["ClipboardPaste","ClipboardPaste method [Tablet PC]","ClipboardPaste method [Tablet PC]","IInkDisp interface","IInkDisp interface [Tablet PC]","ClipboardPaste method","IInkDisp.ClipboardPaste","IInkDisp::ClipboardPaste","c2760791-4238-45a9-a561-a48a55d6444b","msinkaut/IInkDisp::ClipboardPaste","tablet.inkdisp_clipboardpaste"]
old-location: tablet\inkdisp_clipboardpaste.htm
tech.root: tablet
ms.assetid: c2760791-4238-45a9-a561-a48a55d6444b
ms.date: 12/05/2018
ms.keywords: ClipboardPaste, ClipboardPaste method [Tablet PC], ClipboardPaste method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ClipboardPaste method, IInkDisp.ClipboardPaste, IInkDisp::ClipboardPaste, c2760791-4238-45a9-a561-a48a55d6444b, msinkaut/IInkDisp::ClipboardPaste, tablet.inkdisp_clipboardpaste
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
 - IInkDisp::ClipboardPaste
 - msinkaut/IInkDisp::ClipboardPaste
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
 - IInkDisp.ClipboardPaste
---

# IInkDisp::ClipboardPaste


## -description

Copies the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> from the Clipboard to the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

## -parameters

### -param x [in, optional]

Optional. Specifies the x-coordinate to paste to in <b>ink space</b> coordinates. The default value is 0.

### -param y [in, optional]

Optional. Specifies the y-coordinate to paste to in ink space coordinates. The default value is 0.

### -param DataObject [in, optional]

Optional. Specifies the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> to be used. To paste from the Clipboard, set to <b>NULL</b>. The default value is <b>NULL</b>.

### -param Strokes [out, retval]

When this method returns, contains a pointer to the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection in the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object.

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

An error is returned if an unexpected error occurs while accessing the <a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>. If no error occurs but the Clipboard does not contain a format that can be pasted into <b>ink</b> -either <b>ink serialized format (ISF)</b> or a <b>text ink object (tInk)</b> -then <b>NULL</b> is returned and no exception is thrown.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
