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
 

 

