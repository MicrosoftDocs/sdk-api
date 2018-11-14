---
UID: NF:msinkaut.IInkWordList.AddWord
title: IInkWordList::AddWord
author: windows-sdk-content
description: Adds a single word to the InkWordList object.
old-location: tablet\inkwordlist_addword.htm
tech.root: tablet
ms.assetid: bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AddWord, AddWord method [Tablet PC], AddWord method [Tablet PC],IInkWordList interface, AddWord method [Tablet PC],InkWordList class, IInkWordList, IInkWordList interface [Tablet PC],AddWord method, IInkWordList.AddWord, IInkWordList::AddWord, InkWordList class [Tablet PC],AddWord method, bc1a5901-9a31-4f1b-bdbb-47316d0ab9e4, msinkaut/IInkWordList::AddWord, tablet.inkwordlist_addword
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
 - IInkWordList.AddWord
 - InkWordList.AddWord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkWordList.AddWord
: 
---

# IInkWordList::AddWord


## -description



Adds a single word to the <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a> object.




## -parameters




### -param NewWord [in]

The word to add to an <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList</a> object. The word is not added if it already exists in the list.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The word already exists in the list.

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



If a string is added to a word list, its capitalized versions are also implicitly added. For instance, adding "hello" implicitly adds "Hello" and "HELLO".




## -see-also




<a href="https://msdn.microsoft.com/4E872C5A-1223-48EB-9B7D-04B3ADB84B2B">IInkWordList</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">InkWordList Class</a>



<a href="https://msdn.microsoft.com/8bb88cad-7c63-4c2f-9aa1-96eae3a2e89d">RemoveWord Method</a>
 

 

