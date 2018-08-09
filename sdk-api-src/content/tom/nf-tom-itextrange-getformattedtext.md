---
UID: NF:tom.ITextRange.GetFormattedText
title: ITextRange::GetFormattedText
author: windows-sdk-content
description: Gets an ITextRange object with the specified range's formatted text.
old-location: controls\ITextRange_GetFormattedText.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getformattedtext.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFormattedText, GetFormattedText method [Windows Controls], GetFormattedText method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetFormattedText method, ITextRange.GetFormattedText, ITextRange::GetFormattedText, _win32_ITextRange_GetFormattedText, _win32_ITextRange_GetFormattedText_cpp, controls.ITextRange_GetFormattedText, controls._win32_ITextRange_GetFormattedText, tom/ITextRange::GetFormattedText
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
 - ITextRange.GetFormattedText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::GetFormattedText


## -description


Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> object with the specified range's formatted text.


## -parameters




### -param ppRange

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>**</b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> object with the formatted text. 


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
<i>ppRange</i> is null.

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



This method, which amounts to an alias for the <a href="https://msdn.microsoft.com/en-us/library/Bb787840(v=VS.85).aspx">ITextRange::GetDuplicate</a> method, is included to be Microsoft Visual Basic for Applications (VBA)-friendly. The method returns the formatted text in a range. If the <a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a> does not belong to the same Text Object Model (TOM) engine, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> for an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface. 

Among the formats typically supported by <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> are <b>CF_TEXT</b> and <b>CF_RTF</b>. In addition, private formats can be used to reference a text solution's own internal rich-text formats. The following Microsoft Visual Basic example uses the <b>FormattedText</b> property to replace the text in a range2, by the formatted text in range1. 
            

<code>range2.FormattedText = range1.FormattedText</code>




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774149(v=VS.85).aspx">SetFormattedText</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

