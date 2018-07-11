---
UID: NF:tom.ITextDocument.GetStoryCount
title: ITextDocument::GetStoryCount
author: windows-sdk-content
description: Gets the count of stories in this document.
old-location: controls\ITextDocument_GetStoryCount.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstorycount.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetStoryCount, GetStoryCount method [Windows Controls], GetStoryCount method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetStoryCount method, ITextDocument.GetStoryCount, ITextDocument::GetStoryCount, _win32_ITextDocument_GetStoryCount, _win32_ITextDocument_GetStoryCount_cpp, controls.ITextDocument_GetStoryCount, controls._win32_ITextDocument_GetStoryCount, tom/ITextDocument::GetStoryCount
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
 - ITextDocument.GetStoryCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::GetStoryCount


## -description


Gets the count of stories in this document.


## -parameters




### -param pCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The number of stories in the document. 


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



Rich edit controls have only one story and do not implement the <a href="https://msdn.microsoft.com/library/Bb774029(v=VS.85).aspx">ITextDocument::GetStoryRanges</a> method. To avoid getting an error when there is only one story, use <b>ITextDocument::GetStoryCount</b> to check the story count. If the story count is greater than one, then call 
				<b>ITextDocument::GetStoryRanges</b>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774029(v=VS.85).aspx">GetStoryRanges</a>



<a href="https://msdn.microsoft.com/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

