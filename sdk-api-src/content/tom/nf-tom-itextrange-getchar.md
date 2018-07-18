---
UID: NF:tom.ITextRange.GetChar
title: ITextRange::GetChar
author: windows-sdk-content
description: Gets the character at the start position of the range.
old-location: controls\ITextRange_GetChar.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getchar.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetChar, GetChar method [Windows Controls], GetChar method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetChar method, ITextRange.GetChar, ITextRange::GetChar, _win32_ITextRange_GetChar, _win32_ITextRange_GetChar_cpp, controls.ITextRange_GetChar, controls._win32_ITextRange_GetChar, tom/ITextRange::GetChar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITextRange.GetChar
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetChar


## -description


Gets the character at the start position of the range.


## -parameters




### -param pChar

Type: <b>long*</b>

The start character position of the range. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pChar</i> is null, the method fails and it returns E_INVALIDARG.




## -remarks



The following Microsoft Visual Basic example sets <i>ch</i> equal to the character at the start of the range.

    			

<code>ch = r.Char</code>

Similarly, <a href="https://msdn.microsoft.com/b9b68294-906a-4a0e-a770-ac54f7f74961">ITextRange::SetChar</a> overwrites the character at the start of the range with the specified character. The characters retrieved and set by these methods are <b>LONG</b> variables, which hide the way that they are stored in the backing store (as bytes, words, variable-length, and so forth), and they do not require using a <b>BSTR</b>.

The Char property, which can do most things that a characters collection can, has two big advantages: 

<ul>
<li>It can reference any character in the parent story instead of being limited to the parent range. </li>
<li>It is significantly faster, since <b>LONG</b>s are involved instead of range objects. </li>
</ul>
Accordingly, the Text Object Model (TOM) does not support a characters collection.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/b9b68294-906a-4a0e-a770-ac54f7f74961">SetChar</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

