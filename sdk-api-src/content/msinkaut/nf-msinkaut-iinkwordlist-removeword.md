---
UID: NF:msinkaut.IInkWordList.RemoveWord
title: IInkWordList::RemoveWord
author: windows-sdk-content
description: Removes a single word from an InkWordList.
old-location: tablet\inkwordlist_removeword.htm
tech.root: tablet
ms.assetid: 8bb88cad-7c63-4c2f-9aa1-96eae3a2e89d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 8bb88cad-7c63-4c2f-9aa1-96eae3a2e89d, IInkWordList, IInkWordList interface [Tablet PC],RemoveWord method, IInkWordList.RemoveWord, IInkWordList::RemoveWord, InkWordList class [Tablet PC],RemoveWord method, RemoveWord, RemoveWord method [Tablet PC], RemoveWord method [Tablet PC],IInkWordList interface, RemoveWord method [Tablet PC],InkWordList class, msinkaut/IInkWordList::RemoveWord, tablet.inkwordlist_removeword
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkWordList.RemoveWord
 - InkWordList.RemoveWord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkWordList::RemoveWord


## -description



Removes a single word from an <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a>.




## -parameters




### -param RemoveWord [in]

The word to remove from the <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a>.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -remarks



If a string is added to a word list, its capitalized versions are also implicitly added. For instance, adding "hello" implicitly adds "Hello" and "HELLO". Therefore, removing "hello" also implicitly removes "Hello" and "HELLO". However, if you add "hello" and then try to remove "Hello", the <b>RemoveWord</b> call has no effect, because "Hello" was never explicitly added.




## -see-also




<a href="https://msdn.microsoft.com/bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4">AddWord Method</a>



<a href="https://msdn.microsoft.com/4E872C5A-1223-48EB-9B7D-04B3ADB84B2B">IInkWordList</a>



<a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList Class</a>
 

 

