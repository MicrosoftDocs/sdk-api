---
UID: NF:tom.ITextDocument.GetStoryRanges
title: ITextDocument::GetStoryRanges (tom.h)
author: windows-sdk-content
description: Gets the story collection object used to enumerate the stories in a document.
old-location: controls\ITextDocument_GetStoryRanges.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstoryranges.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStoryRanges, GetStoryRanges method [Windows Controls], GetStoryRanges method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetStoryRanges method, ITextDocument.GetStoryRanges, ITextDocument::GetStoryRanges, _win32_ITextDocument_GetStoryRanges, _win32_ITextDocument_GetStoryRanges_cpp, controls.ITextDocument_GetStoryRanges, controls._win32_ITextDocument_GetStoryRanges, tom/ITextDocument::GetStoryRanges
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument.GetStoryRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::GetStoryRanges


## -description


Gets the story collection object used to enumerate the stories in a document. 


## -parameters




### -param ppStories

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774062(v=VS.85).aspx">ITextStoryRanges</a>**</b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb774062(v=VS.85).aspx">ITextStoryRanges</a> pointer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented; only one story in this document.

</td>
</tr>
</table>
 




## -remarks



Invoke this method only if <a href="https://msdn.microsoft.com/en-us/library/Bb774027(v=VS.85).aspx">ITextDocument::GetStoryCount</a> returns a value greater than 1.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774027(v=VS.85).aspx">GetStoryCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774062(v=VS.85).aspx">ITextStoryRanges</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

