---
UID: NF:tom.ITextRange.SetFormattedText
title: ITextRange::SetFormattedText
author: windows-sdk-content
description: Sets the formatted text of this range text to the formatted text of the specified range.
old-location: controls\ITextRange_SetFormattedText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setformattedtext.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextRange interface [Windows Controls],SetFormattedText method, ITextRange.SetFormattedText, ITextRange::SetFormattedText, SetFormattedText, SetFormattedText method [Windows Controls], SetFormattedText method [Windows Controls],ITextRange interface, _win32_ITextRange_SetFormattedText, _win32_ITextRange_SetFormattedText_cpp, controls.ITextRange_SetFormattedText, controls._win32_ITextRange_SetFormattedText, tom/ITextRange::SetFormattedText
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
 - ITextRange.SetFormattedText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::SetFormattedText


## -description


Sets the formatted text of this range text to the formatted text of the specified range.


## -parameters




### -param pRange [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>*</b>

The formatted text to replace this range's text. 


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRange</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



If the <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> does not belong to the same Text Object Model (TOM) engine, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> for an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface.

Among the formats typically supported by the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> are CF_TEXT and CF_RTF. In addition, private formats can be used to reference a text solution's own internal rich-text formats. The following Microsoft Visual Basic example uses the <b>FormattedText</b> property to replace the text in range2 with the formatted text in range1.

<code>range2.FormattedText = range1.FormattedText</code>




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787840(v=VS.85).aspx">GetDuplicate</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773958(v=VS.85).aspx">GetFormattedText</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

