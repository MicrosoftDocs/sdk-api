---
UID: NF:tom.ITextRange.SetIndex
title: ITextRange::SetIndex
author: windows-sdk-content
description: Changes this range to the specified unit of the story.
old-location: controls\ITextRange_SetIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setindex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextRange interface [Windows Controls],SetIndex method, ITextRange.SetIndex, ITextRange::SetIndex, SetIndex, SetIndex method [Windows Controls], SetIndex method [Windows Controls],ITextRange interface, _win32_ITextRange_SetIndex, _win32_ITextRange_SetIndex_cpp, controls.ITextRange_SetIndex, controls._win32_ITextRange_SetIndex, tom/ITextRange::SetIndex
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
 - ITextRange.SetIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::SetIndex


## -description


Changes this range to the specified unit of the story. 


## -parameters




### -param Unit [in]

Type: <b>long</b>

Unit used to index the range. For a list of unit values, see <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>. 


### -param Index [in]

Type: <b>long</b>

Index for the <i>Unit</i>. This range is relocated to the <i>Unit</i> that has this index number. If positive, the numbering of <i>Unit</i>s begins at the start of the story and proceeds forward. If negative, the numbering begins at the end of the story and proceeds backward. The start of the story corresponds to an <i>Index</i> of 1 for all units that exist, and the last unit in the story corresponds to an <i>Index</i> of -1. 


### -param Extend [in]

Type: <b>long</b>

Flag that indicates the extent of the range. If zero (the default), the range is collapsed to an insertion point at the start position of the specified <i>Unit</i>. If nonzero, the range is set to the entire <i>Unit</i>. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Index is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -remarks



This method allows an application to work with line-oriented text, such as programs, in a convenient way. For example, <code>SetIndex(tomLine, 10, 0)</code> converts a range to an insertion point at the start of the tenth line.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

