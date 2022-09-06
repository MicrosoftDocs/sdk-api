---
UID: NE:msinkaut.InkClipboardFormats
title: InkClipboardFormats (msinkaut.h)
description: Specifies the format of ink that is stored on the Clipboard.
helpviewer_keywords: ["ICF_Bitmap","ICF_CopyMask","ICF_Default","ICF_EnhancedMetafile","ICF_InkSerializedFormat","ICF_Metafile","ICF_None","ICF_PasteMask","ICF_SketchInk","ICF_TextInk","InkClipboardFormatFlags","InkClipboardFormatFlags enumeration [Tablet PC]","InkClipboardFormats","InkClipboardFormats enumeration [Tablet PC]","bedee31c-d957-4162-83d9-f1c8df9428cd","msinkaut/ICF_Bitmap","msinkaut/ICF_CopyMask","msinkaut/ICF_Default","msinkaut/ICF_EnhancedMetafile","msinkaut/ICF_InkSerializedFormat","msinkaut/ICF_Metafile","msinkaut/ICF_None","msinkaut/ICF_PasteMask","msinkaut/ICF_SketchInk","msinkaut/ICF_TextInk","msinkaut/InkClipboardFormats","tablet.inkclipboardformats"]
old-location: tablet\inkclipboardformats.htm
tech.root: tablet
ms.assetid: bedee31c-d957-4162-83d9-f1c8df9428cd
ms.date: 12/05/2018
ms.keywords: ICF_Bitmap, ICF_CopyMask, ICF_Default, ICF_EnhancedMetafile, ICF_InkSerializedFormat, ICF_Metafile, ICF_None, ICF_PasteMask, ICF_SketchInk, ICF_TextInk, InkClipboardFormatFlags, InkClipboardFormatFlags enumeration [Tablet PC], InkClipboardFormats, InkClipboardFormats enumeration [Tablet PC], bedee31c-d957-4162-83d9-f1c8df9428cd, msinkaut/ICF_Bitmap, msinkaut/ICF_CopyMask, msinkaut/ICF_Default, msinkaut/ICF_EnhancedMetafile, msinkaut/ICF_InkSerializedFormat, msinkaut/ICF_Metafile, msinkaut/ICF_None, msinkaut/ICF_PasteMask, msinkaut/ICF_SketchInk, msinkaut/ICF_TextInk, msinkaut/InkClipboardFormats, tablet.inkclipboardformats
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
req.typenames: InkClipboardFormats
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkClipboardFormats
 - msinkaut/InkClipboardFormats
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
 - InkClipboardFormatFlags
---

# InkClipboardFormats enumeration


## -description

Specifies the format of ink that is stored on the Clipboard.

## -enum-fields

### -field ICF_None:0

 A flag that can be used to verify whether any formats are present by checking against it.

### -field ICF_InkSerializedFormat:0x1

Ink is encoded in ink serialized format (ISF). This is the most compact persistent representation of ink. Although it often contains only ink data, ISF is extensible. Applications can set custom attributes (identified by a globally unique identifier (GUID)) on an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object, stroke, or point. This allows an application to store any kind of data or metadata that it requires as an attribute in an ISF stream.

### -field ICF_SketchInk:0x2

Ink is not expected to form words, but rather is interpreted as a picture. This is also useful for representing multiple words.

### -field ICF_TextInk:0x6

Ink is expected to form words. It enables the recognizer to convert the ink to text. The recognized text is either the recognition alternate with the greatest confidence rating or another alternate chosen from a list. This is useful for representing a single word.

### -field ICF_EnhancedMetafile:0x8

The enhanced metafile to play to create the background. The metafile must remain valid for as long as it is used to render the ink background.

### -field ICF_Metafile:0x20

Ink is stored as a metafile or a list of commands that can be played back to draw a graphic.

### -field ICF_Bitmap:0x40

The bitmap to use as the background. The bitmap device context must remain valid for as long as it is used to render the ink background.

### -field ICF_PasteMask:0x7

The formats that can be used for pasting, including <a href="/windows/desktop/tablet/sink-and-tink-objects">tInk</a>, sInk, and ISF.

### -field ICF_CopyMask:0x7f

The formats that are copied to the Clipboard through ink.

This is the default value.

### -field ICF_Default

Ink is stored as a CopyMask.

## -remarks

In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy">ClipboardCopy Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle">ClipboardCopyWithRectangle Method</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/sink-and-tink-objects">sInk and tInk Objects</a>
