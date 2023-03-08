---
UID: NN:tom.ITextSelection
title: ITextSelection (tom.h)
description: A text selection is a text range with selection highlighting.
helpviewer_keywords: ["ITextSelection","ITextSelection interface [Windows Controls]","ITextSelection interface [Windows Controls]","described","_win32_ITextSelection","_win32_ITextSelection_cpp","controls.ITextSelection","controls._win32_ITextSelection","tom/ITextSelection"]
old-location: controls\ITextSelection.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextselection.htm
ms.date: 12/05/2018
ms.keywords: ITextSelection, ITextSelection interface [Windows Controls], ITextSelection interface [Windows Controls],described, _win32_ITextSelection, _win32_ITextSelection_cpp, controls.ITextSelection, controls._win32_ITextSelection, tom/ITextSelection
req.header: tom.h
req.include-header: 
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextSelection
 - tom/ITextSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextSelection
---

# ITextSelection interface


## -description

A text selection is a text range with selection highlighting.

## -inheritance

The <b>ITextSelection</b> interface inherits from <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>. <b>ITextSelection</b> also has these types of members:

## -remarks

The selection is associated with some kind of view, and has some UI-oriented methods that allow one to emulate keyboard input. Thus, an application can use the <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> methods on a text selection, as well as the <b>ITextSelection</b> methods.

For keyboard input emulation, ranges used in selections use the concept of the <i>active end</i>, which is typically the end that was last moved. For example, if an <b>ITextRange::Move</b>* method operates on a range that is actually a text selection, the most recently moved end is the active one. The most familiar examples of the active end are those involving Shift+Arrow Key handling, where the active end is the one that moves. Accordingly, the <b>ITextSelection</b> methods include move methods for the active end, such as <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a> or <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a>, and methods to get and set the active end status. These methods manipulate selections in ways similar to the standard cursor-keypad operations. This allows you to implement, for example, a macro recorder facility.

To see how the cursor-keypad methods work, see the following table. A given method corresponds to a cursor-keypad key with the Ctrl and Shift keys. The <i>Unit</i> parameter is selected by pressing or not pressing the Ctrl key, while the <i>Extend</i> parameter is selected by pressing or not pressing the Shift key. Note, <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveup">MoveUp</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-movedown">MoveDown</a> correspond to more than one keypad key. For more information, see the descriptions of the methods.

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

Applications can retrieve an <b>ITextSelection</b> pointer by calling the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-getselection">GetSelection</a> method.
