---
UID: NF:tom.ITextStoryRanges._NewEnum
title: ITextStoryRanges::_NewEnum
author: windows-sdk-content
description: Retrieves an IEnumVARIANT enumerator interface for this collection of stories.
old-location: controls\ITextStoryRanges__NewEnum.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\_newenum.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoryRanges interface [Windows Controls],_NewEnum method, ITextStoryRanges._NewEnum, ITextStoryRanges::_NewEnum, _NewEnum, _NewEnum method [Windows Controls], _NewEnum method [Windows Controls],ITextStoryRanges interface, _win32_ITextStoryRanges__NewEnum, _win32_ITextStoryRanges__NewEnum_cpp, controls.ITextStoryRanges__NewEnum, controls._win32_ITextStoryRanges__NewEnum, tom/ITextStoryRanges::_NewEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITextStoryRanges._NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoryRanges::_NewEnum


## -description


Retrieves an 
			<b>IEnumVARIANT</b> enumerator interface for this collection of stories.


## -parameters




### -param ppunkEnum

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The pointer to the enumerator interface. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppunkEnum</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -remarks



This definition together with the implementation of 
				<b>IEnumVARIANT</b>, enables one to support the following Microsoft Visual Basic for Applications (VBA) code.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    Dim t As ITextDocument
    Dim c As ITextStoryRanges
    Dim r As ITextRange

    Set t = gObj
    Set c = t.StoryRanges

    For Each r In c
        Debug.Print r.Text
    Next</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/eee6c992-1f6a-4e4e-bd8a-34a9aff41859">ITextStoryRanges</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

