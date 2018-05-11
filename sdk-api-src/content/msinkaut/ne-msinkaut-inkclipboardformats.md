---
UID: NE:msinkaut.InkClipboardFormats
title: InkClipboardFormats
author: windows-driver-content
description: Specifies the format of ink that is stored on the Clipboard.
old-location: tablet\inkclipboardformats.htm
old-project: tablet
ms.assetid: bedee31c-d957-4162-83d9-f1c8df9428cd
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICF_Bitmap, ICF_CopyMask, ICF_Default, ICF_EnhancedMetafile, ICF_InkSerializedFormat, ICF_Metafile, ICF_None, ICF_PasteMask, ICF_SketchInk, ICF_TextInk, InkClipboardFormatFlags, InkClipboardFormatFlags enumeration [Tablet PC], InkClipboardFormats, InkClipboardFormats enumeration [Tablet PC], bedee31c-d957-4162-83d9-f1c8df9428cd, msinkaut/ICF_Bitmap, msinkaut/ICF_CopyMask, msinkaut/ICF_Default, msinkaut/ICF_EnhancedMetafile, msinkaut/ICF_InkSerializedFormat, msinkaut/ICF_Metafile, msinkaut/ICF_None, msinkaut/ICF_PasteMask, msinkaut/ICF_SketchInk, msinkaut/ICF_TextInk, msinkaut/InkClipboardFormats, tablet.inkclipboardformats
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: InkClipboardFormats
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msinkaut.h
api_name:
-	InkClipboardFormatFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# InkClipboardFormats enumeration


## -description



Specifies the format of ink that is stored on the Clipboard.




## -enum-fields




### -field ICF_None

 A flag that can be used to verify whether any formats are present by checking against it.


### -field ICF_InkSerializedFormat

Ink is encoded in ink serialized format (ISF). This is the most compact persistent representation of ink. Although it often contains only ink data, ISF is extensible. Applications can set custom attributes (identified by a globally unique identifier (GUID)) on an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object, stroke, or point. This allows an application to store any kind of data or metadata that it requires as an attribute in an ISF stream.


### -field ICF_SketchInk

Ink is not expected to form words, but rather is interpreted as a picture. This is also useful for representing multiple words.


### -field ICF_TextInk

Ink is expected to form words. It enables the recognizer to convert the ink to text. The recognized text is either the recognition alternate with the greatest confidence rating or another alternate chosen from a list. This is useful for representing a single word.


### -field ICF_EnhancedMetafile

The enhanced metafile to play to create the background. The metafile must remain valid for as long as it is used to render the ink background.


### -field ICF_Metafile

Ink is stored as a metafile or a list of commands that can be played back to draw a graphic.


### -field ICF_Bitmap

The bitmap to use as the background. The bitmap device context must remain valid for as long as it is used to render the ink background.


### -field ICF_PasteMask

The formats that can be used for pasting, including <a href="https://msdn.microsoft.com/fbd7bdf0-63b4-48d1-be91-eabbbb3f1618">tInk</a>, sInk, and ISF.


### -field ICF_CopyMask

The formats that are copied to the Clipboard through ink.

This is the default value.


### -field ICF_Default

Ink is stored as a CopyMask.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.




## -see-also




<a href="https://msdn.microsoft.com/ad62c9b3-6df6-445b-9085-7cd5c4b6b31f">ClipboardCopy Method</a>



<a href="https://msdn.microsoft.com/a4e6a183-242a-40af-871b-43a0b177a27a">ClipboardCopyWithRectangle Method</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/fbd7bdf0-63b4-48d1-be91-eabbbb3f1618">sInk and tInk Objects</a>
 

 

