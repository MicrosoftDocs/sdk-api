---
UID: NN:ctffunc.ITfFnGetPreferredTouchKeyboardLayout
title: ITfFnGetPreferredTouchKeyboardLayout
author: windows-sdk-content
description: The ITfFnGetPreferredTouchKeyboardLayout interface is implemented by a text service to specify the use of a particular keyboard layout supported by the inbox Windows 8 touch keyboard.
old-location: tsf\itffngetpreferredtouchkeyboardlayout.htm
tech.root: TSF
ms.assetid: 1BC4A446-AEDC-44AA-9BD7-786917AD2556
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnGetPreferredTouchKeyboardLayout, ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework], ITfFnGetPreferredTouchKeyboardLayout interface [Text Services Framework],described, ctffunc/ITfFnGetPreferredTouchKeyboardLayout, tsf.itffngetpreferredtouchkeyboardlayout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnGetPreferredTouchKeyboardLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITfFnGetPreferredTouchKeyboardLayout interface


## -description


The <b>ITfFnGetPreferredTouchKeyboardLayout</b> interface is implemented by a text service to specify the use of a particular keyboard layout supported by the inbox Windows 8 touch keyboard.

When an IME is active the touch keyboard will use <a href="https://msdn.microsoft.com/en-us/library/ms538981(v=VS.85).aspx">ITfFunctionProvider::GetFunction</a> with <b>IID_ITfFnGetPreferredTouchKeyboardLayout</b> to query the IME for this function.

If the function is not supported by the IME, then the touch keyboard will show the default layout for the language.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnGetPreferredTouchKeyboardLayout</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms538978(v=VS.85).aspx">ITfFunction</a>. <b>ITfFnGetPreferredTouchKeyboardLayout</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh802865(v=VS.85).aspx">GetLayout</a>
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




<a href="https://msdn.microsoft.com/en-us/library/ms538978(v=VS.85).aspx">ITfFunction</a>
 

 

