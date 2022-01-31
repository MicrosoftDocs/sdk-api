---
UID: NE:msinkaut.InkClipboardModes
title: InkClipboardModes (msinkaut.h)
description: Specifies the copy options of the Clipboard.
helpviewer_keywords: ["ICB_Copy","ICB_Cut","ICB_Default","ICB_DelayedCopy","ICB_ExtractOnly","InkClipboardModes","InkClipboardModes enumeration [Tablet PC]","a9718b79-8f98-4bfc-a5db-208899d1f59e","msinkaut/ICB_Copy","msinkaut/ICB_Cut","msinkaut/ICB_Default","msinkaut/ICB_DelayedCopy","msinkaut/ICB_ExtractOnly","msinkaut/InkClipboardModes","tablet.inkclipboardmodes"]
old-location: tablet\inkclipboardmodes.htm
tech.root: tablet
ms.assetid: a9718b79-8f98-4bfc-a5db-208899d1f59e
ms.date: 12/05/2018
ms.keywords: ICB_Copy, ICB_Cut, ICB_Default, ICB_DelayedCopy, ICB_ExtractOnly, InkClipboardModes, InkClipboardModes enumeration [Tablet PC], a9718b79-8f98-4bfc-a5db-208899d1f59e, msinkaut/ICB_Copy, msinkaut/ICB_Cut, msinkaut/ICB_Default, msinkaut/ICB_DelayedCopy, msinkaut/ICB_ExtractOnly, msinkaut/InkClipboardModes, tablet.inkclipboardmodes
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: InkClipboardModes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkClipboardModes
 - msinkaut/InkClipboardModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkClipboardModes
---

# InkClipboardModes enumeration


## -description

Specifies the copy options of the Clipboard.

## -enum-fields

### -field ICB_Copy:0

The ink is copied to the Clipboard.

### -field ICB_Cut:0x1

The ink is cut and copied to the Clipboard.

### -field ICB_ExtractOnly:0x30

The ink is not copied to the Clipboard. Typically, use this option if you want to add something else, such as text, to the ink before you copy it to the Clipboard.

### -field ICB_DelayedCopy:0x20

 Delayed rendering is used to reduce the amount of data that is stored on the Clipboard. The data is rendered when a paste request is made.

### -field ICB_Default:ICB_Copy

Copy mode is used to copy the Ink.

## -remarks

You can use the DelayedCopy flag to interact directly with the data object and add additional formats to the clipboard.

<div class="alert"><b>Caution</b>  To avoid potential memory leaks as a result of using the <b>DelayedCopy</b> flag, you must call the <a href="/windows/desktop/api/ole2/nf-ole2-oleflushclipboard">OleFlushClipboard</a> or <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> method. This must be done before the application exits if the last call to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy">ClipboardCopy</a> method used the <b>DelayedCopy</b> flag.</div>
<div> </div>
To remove the pointer from the clipboard, the parameter for the <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> should be <b>NULL</b>. For the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idataobjectprovider-setdataobject">SetDataObject</a> method, the <i>data</i> parameter should be <b>NULL</b>, and the <i>copy</i> parameter should be <b>TRUE</b>.

The <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idataobjectprovider-setdataobject">SetDataObject</a> methods replace the contents of the clipboard.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy">ClipboardCopy Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle">ClipboardCopyWithRectangle Method</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
