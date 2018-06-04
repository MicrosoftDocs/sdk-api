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

# InkClipboardModes enumeration


## -description



Specifies the copy options of the Clipboard.




## -enum-fields




### -field ICB_Copy

The ink is copied to the Clipboard.


### -field ICB_Cut

The ink is cut and copied to the Clipboard.


### -field ICB_ExtractOnly

The ink is not copied to the Clipboard. Typically, use this option if you want to add something else, such as text, to the ink before you copy it to the Clipboard.


### -field ICB_DelayedCopy

 Delayed rendering is used to reduce the amount of data that is stored on the Clipboard. The data is rendered when a paste request is made.


### -field ICB_Default

Copy mode is used to copy the Ink.


## -remarks



You can use the DelayedCopy flag to interact directly with the data object and add additional formats to the clipboard.

<div class="alert"><b>Caution</b>  To avoid potential memory leaks as a result of using the <b>DelayedCopy</b> flag, you must call the <a href="_ole_OleFlushClipboard">OleFlushClipboard</a> or <a href="_ole_OleSetClipboard">OleSetClipboard</a> method. This must be done before the application exits if the last call to the <a href="https://msdn.microsoft.com/ad62c9b3-6df6-445b-9085-7cd5c4b6b31f">ClipboardCopy</a> method used the <b>DelayedCopy</b> flag.</div>
<div> </div>
To remove the pointer from the clipboard, the parameter for the <a href="_ole_OleSetClipboard">OleSetClipboard</a> should be <b>NULL</b>. For the <a href="frlrfSystemWindowsFormsClipboardClassSetDataObjectTopic">SetDataObject</a> method, the <i>data</i> parameter should be <b>NULL</b>, and the <i>copy</i> parameter should be <b>TRUE</b>.

The <a href="_ole_OleSetClipboard">OleSetClipboard</a> and <a href="frlrfSystemWindowsFormsClipboardClassSetDataObjectTopic">SetDataObject</a> methods replace the contents of the clipboard.




## -see-also




<a href="https://msdn.microsoft.com/ad62c9b3-6df6-445b-9085-7cd5c4b6b31f">ClipboardCopy Method</a>



<a href="https://msdn.microsoft.com/a4e6a183-242a-40af-871b-43a0b177a27a">ClipboardCopyWithRectangle Method</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

