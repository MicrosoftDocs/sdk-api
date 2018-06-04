---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

