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

# ITfFnGetPreferredTouchKeyboardLayout interface


## -description


The <b>ITfFnGetPreferredTouchKeyboardLayout</b> interface is implemented by a text service to specify the use of a particular keyboard layout supported by the inbox Windows 8 touch keyboard.

When an IME is active the touch keyboard will use <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with <b>IID_ITfFnGetPreferredTouchKeyboardLayout</b> to query the IME for this function.

If the function is not supported by the IME, then the touch keyboard will show the default layout for the language.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnGetPreferredTouchKeyboardLayout</b> interface inherits from <a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction</a>. <b>ITfFnGetPreferredTouchKeyboardLayout</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnGetPreferredTouchKeyboardLayout</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03C14744-A4A3-4C62-8E7F-CDCC638BBCA1">GetLayout</a>
</td>
<td align="left" width="63%">
Obtains the touch keyboard layout identifier of the layout that the IME directs the touch keyboard to show while the IME is active.

</td>
</tr>
</table> 


## -remarks



For more information on the layouts which can be specified, see GetLayout.

This interface applies only to IMEs written using the Text Services Framework and not to legacy IMM32 IMEs, and it only applies to the following input languages:

<ul>
<li>Japanese</li>
<li>Korean</li>
<li>Simplified Chinese</li>
<li>Traditional Chinese</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/140b1ed8-8876-4f06-8ed2-7b0dccdc0a69">ITfFunction</a>
 

 

