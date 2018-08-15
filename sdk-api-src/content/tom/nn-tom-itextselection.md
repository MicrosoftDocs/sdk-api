---
UID: NN:tom.ITextSelection
title: ITextSelection
author: windows-sdk-content
description: A text selection is a text range with selection highlighting.
old-location: controls\ITextSelection.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextselection.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextSelection, ITextSelection interface [Windows Controls], ITextSelection interface [Windows Controls],described, _win32_ITextSelection, _win32_ITextSelection_cpp, controls.ITextSelection, controls._win32_ITextSelection, tom/ITextSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextSelection interface


## -description


A text selection is a text range with selection highlighting.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextSelection</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>. <b>ITextSelection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextSelection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787752(v=VS.85).aspx">EndKey</a>
</td>
<td align="left" width="63%">
Mimics the functionality of the End key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3100b62-a3f1-4d4b-85d2-df06c20ebd70">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the text selection flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85d4a3f0-855e-4d24-9686-3d4e62743356">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of text selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774044(v=VS.85).aspx">HomeKey</a>
</td>
<td align="left" width="63%">
Generalizes the functionality of the Home key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774066(v=VS.85).aspx">MoveDown</a>
</td>
<td align="left" width="63%">
Mimics the functionality of the Down Arrow and Page Down keys. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774074(v=VS.85).aspx">MoveLeft</a>
</td>
<td align="left" width="63%">
Generalizes the functionality of the Left Arrow key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774076(v=VS.85).aspx">MoveRight</a>
</td>
<td align="left" width="63%">
Generalizes the functionality of the Right Arrow key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774087(v=VS.85).aspx">MoveUp</a>
</td>
<td align="left" width="63%">
Mimics the functionality of the  Up Arrow and Page Up keys. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4b96d2a-2e75-4459-9a6e-5e0483926ce1">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the text selection flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787836(v=VS.85).aspx">TypeText</a>
</td>
<td align="left" width="63%">
Types the string given by <i>bstr</i> at this selection as if someone typed it. This is similar to the underlying <a href="https://msdn.microsoft.com/en-us/library/Bb787831(v=VS.85).aspx">SetText</a> method, but is sensitive to the Insert/Overtype key state and UI settings like AutoCorrect and smart quotes.

</td>
</tr>
</table> 


## -remarks



The selection is associated with some kind of view, and has some UI-oriented methods that allow one to emulate keyboard input. Thus, an application can use the <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> methods on a text selection, as well as the <b>ITextSelection</b> methods.

For keyboard input emulation, ranges used in selections use the concept of the <i>active end</i>, which is typically the end that was last moved. For example, if an <b>ITextRange::Move</b>* method operates on a range that is actually a text selection, the most recently moved end is the active one. The most familiar examples of the active end are those involving Shift+Arrow Key handling, where the active end is the one that moves. Accordingly, the <b>ITextSelection</b> methods include move methods for the active end, such as <a href="https://msdn.microsoft.com/en-us/library/Bb774074(v=VS.85).aspx">MoveLeft</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb774076(v=VS.85).aspx">MoveRight</a>, and methods to get and set the active end status. These methods manipulate selections in ways similar to the standard cursor-keypad operations. This allows you to implement, for example, a macro recorder facility.

To see how the cursor-keypad methods work, see the following table. A given method corresponds to a cursor-keypad key with the Ctrl and Shift keys. The <i>Unit</i> parameter is selected by pressing or not pressing the Ctrl key, while the <i>Extend</i> parameter is selected by pressing or not pressing the Shift key. Note, <a href="https://msdn.microsoft.com/en-us/library/Bb774087(v=VS.85).aspx">MoveUp</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774066(v=VS.85).aspx">MoveDown</a> correspond to more than one keypad key. For more information, see the descriptions of the methods.

<table class="clsStd">
<tr>
<th>Method</th>
<th>Cursor-keypad key</th>
<th>Unit given by CTRL pressed (not pressed)</th>
<th>Extend given by SHIFT pressed (not pressed)</th>
</tr>
<tr>
<td>EndKey</td>
<td>End</td>
<td>tomStory (tomLine)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>HomeKey</td>
<td>Home</td>
<td>tomStory (tomLine)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveLeft</td>
<td>Left Arrow</td>
<td>tomWord (tomCharacter)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveRight</td>
<td>Right Arrow</td>
<td>tomWord (tomCharacter)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveUp</td>
<td>Up Arrow</td>
<td>tomParagraph (tomLine)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveDown</td>
<td>Down Arrow</td>
<td>tomParagraph (tomLine)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveUp</td>
<td>Page Up</td>
<td>tomWindow (tomScreen)</td>
<td>tomExtend (tomMove)</td>
</tr>
<tr>
<td>MoveDown</td>
<td>Page Down</td>
<td>tomWindow (tomScreen)</td>
<td>tomExtend (tomMove)</td>
</tr>
</table>
 

Applications typically do not implement the <b>ITextSelection</b> interface. Instead, Microsoft text solutions such as rich edit controls implement <b>ITextSelection</b> as part of their Text Object Model (TOM) implementation.

Applications can retrieve an <b>ITextSelection</b> pointer by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb774013(v=VS.85).aspx">GetSelection</a> method.



