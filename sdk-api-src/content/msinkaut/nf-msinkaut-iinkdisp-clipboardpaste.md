---
UID: NF:msinkaut.IInkDisp.ClipboardPaste
title: IInkDisp::ClipboardPaste
author: windows-sdk-content
description: Copies the IDataObject from the Clipboard to the InkDisp object.
old-location: tablet\inkdisp_clipboardpaste.htm
old-project: tablet
ms.assetid: c2760791-4238-45a9-a561-a48a55d6444b
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: ClipboardPaste, ClipboardPaste method [Tablet PC], ClipboardPaste method [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],ClipboardPaste method, IInkDisp.ClipboardPaste, IInkDisp::ClipboardPaste, c2760791-4238-45a9-a561-a48a55d6444b, msinkaut/IInkDisp::ClipboardPaste, tablet.inkdisp_clipboardpaste
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp::ClipboardPaste


## -description



Copies the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> from the Clipboard to the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -parameters




### -param x [in, optional]

Optional. Specifies the x-coordinate to paste to in <b>ink space</b> coordinates. The default value is 0.


### -param y [in, optional]

Optional. Specifies the y-coordinate to paste to in ink space coordinates. The default value is 0.


### -param DataObject [in, optional]

Optional. Specifies the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> to be used. To paste from the Clipboard, set to <b>NULL</b>. The default value is <b>NULL</b>.


### -param Strokes [out, retval]

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


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



An error is returned if an unexpected error occurs while accessing the <a href="https://msdn.microsoft.com/library/ms648709(v=VS.85).aspx">Clipboard</a>. If no error occurs but the Clipboard does not contain a format that can be pasted into <b>ink</b> -either <b>ink serialized format (ISF)</b> or a <b>text ink object (tInk)</b> -then <b>NULL</b> is returned and no exception is thrown. For more information about the Clipboard, see Clipboard in MSDN&lt;entity type="reg"/&gt;




## -see-also




<a href="tablet.iinkdisp">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes Collection</a>
 

 

