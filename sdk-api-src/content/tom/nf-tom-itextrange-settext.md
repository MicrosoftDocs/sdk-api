---
UID: NF:tom.ITextRange.SetText
title: ITextRange::SetText
author: windows-driver-content
description: Sets the text in this range.
old-location: controls\ITextRange_SetText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\settext.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITextRange interface [Windows Controls],SetText method, ITextRange.SetText, ITextRange::SetText, SetText, SetText method [Windows Controls], SetText method [Windows Controls],ITextRange interface, _win32_ITextRange_SetText, _win32_ITextRange_SetText_cpp, controls.ITextRange_SetText, controls._win32_ITextRange_SetText, tom/ITextRange::SetText
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.SetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::SetText


## -description


Sets the text in this range.


## -parameters




### -param bstr [in]

Type: <b>BSTR</b>

Text that replaces the current text in this range. If null, the current text is deleted. 


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
bstr is null.

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



<b>ITextRange::SetText</b> replaces the text in the range with the new text. In contrast, <a href="https://msdn.microsoft.com/6022717e-6890-46d2-9fbd-bb4ed54dc130">TypeText</a> replaces the selection with the text <i>bstr</i> and leaves the selection as an insertion point just following the inserted text, just as if you had typed the text in. For UI selection behavior, see <b>TypeText</b>.

If, after you call <b>ITextRange::SetText</b>, you call <a href="https://msdn.microsoft.com/8cef8a1c-7b21-43cd-a4dd-b5a579bbfdaf">ITextRange::GetText</a>, you get back the same text that you set with the <b>ITextRange::SetText</b> method (unless some other range has changed that text in between the calls). 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/6022717e-6890-46d2-9fbd-bb4ed54dc130">TypeText</a>
 

 

