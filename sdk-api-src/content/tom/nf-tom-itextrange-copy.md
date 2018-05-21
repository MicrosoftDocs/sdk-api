---
UID: NF:tom.ITextRange.Copy
title: ITextRange::Copy
author: windows-driver-content
description: Copies the text to a data object.
old-location: controls\ITextRange_Copy.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\copy.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: Copy, Copy method [Windows Controls], Copy method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Copy method, ITextRange.Copy, ITextRange::Copy, _win32_ITextRange_Copy, _win32_ITextRange_Copy_cpp, controls.ITextRange_Copy, controls._win32_ITextRange_Copy, tom/ITextRange::Copy
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
-	ITextRange.Copy
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::Copy


## -description


Copies the text to a data object. 


## -parameters




### -param pVar

Type: <b>VARIANT*</b>

The copied text. 
					<i>pVar</i>-&gt;ppunkVal is the out parameter for an 
					<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> provided that the following conditions exist: 
					

<ul>
<li>pVar-&gt;vt = (VT_UNKNOWN | VT_BYREF) </li>
<li>pVar is not null </li>
<li>pVar-&gt;ppunkVal is not null </li>
</ul>
Otherwise, the clipboard is used. 


## -returns



Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise, it returns <b>E_OUTOFMEMORY</b>.




## -remarks



The <a href="https://msdn.microsoft.com/78e00053-8746-4f66-a276-97457e5f2e8e">ITextRange::Cut</a>, 
				<b>ITextRange::Copy</b>, and <a href="https://msdn.microsoft.com/62842b6f-381c-41ac-974e-9e03eae148f7">ITextRange::Paste</a> methods let you perform the usual 
				<b>Cut</b>, <b>Copy</b>, and 
				<b>Paste</b> operations on a range object using an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, thereby not changing the contents of the clipboard. Among clipboard formats typically supported are <b>CF_TEXT</b> and <b>CF_RTF</b>. In addition, private clipboard formats can be used to reference a text solution's own internal rich text formats.

To copy and replace plain text, you can use the <a href="https://msdn.microsoft.com/8cef8a1c-7b21-43cd-a4dd-b5a579bbfdaf">ITextRange::GetText</a> 
				<b></b>and <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">ITextRange::SetText</a> 
				<b></b>methods. To copy formatted text from range r1 to range r2 without using the clipboard, you can use <b>Copy</b> and 
				<b>Paste</b> and also the <a href="https://msdn.microsoft.com/d5985e53-8f17-4a01-b12a-b08c734975fb">ITextRange::GetFormattedText</a> and <a href="https://msdn.microsoft.com/19a974ba-e6ab-4a32-81ee-74172965ddb6">ITextRange::SetFormattedText</a> methods, as shown in the following Microsoft Visual Basic example:

<code>r2.GetFormattedText = r1.GetFormattedText</code>




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/78e00053-8746-4f66-a276-97457e5f2e8e">Cut</a>



<a href="https://msdn.microsoft.com/d5985e53-8f17-4a01-b12a-b08c734975fb">GetFormattedText</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/62842b6f-381c-41ac-974e-9e03eae148f7">Paste</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/19a974ba-e6ab-4a32-81ee-74172965ddb6">SetFormattedText</a>



<a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

