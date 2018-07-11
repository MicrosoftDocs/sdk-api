---
UID: NF:tom.ITextPara.GetPageBreakBefore
title: ITextPara::GetPageBreakBefore
author: windows-sdk-content
description: Determines whether each paragraph in the range must begin on a new page.
old-location: controls\ITextPara_GetPageBreakBefore.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getpagebreakbefore.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: GetPageBreakBefore, GetPageBreakBefore method [Windows Controls], GetPageBreakBefore method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetPageBreakBefore method, ITextPara.GetPageBreakBefore, ITextPara::GetPageBreakBefore, _win32_ITextPara_GetPageBreakBefore, _win32_ITextPara_GetPageBreakBefore_cpp, controls.ITextPara_GetPageBreakBefore, controls._win32_ITextPara_GetPageBreakBefore, tom/ITextPara::GetPageBreakBefore
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
 - ITextPara.GetPageBreakBefore
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetPageBreakBefore


## -description


Determines whether each paragraph in the range must begin on a new page.


## -parameters




### -param pValue






#### - pBool

Type: <b>long*</b>

A variable that is one of the following values: 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomTrue</td>
<td>Each paragraph in this range must begin on a new page.</td>
</tr>
<tr>
<td>tomFalse</td>
<td>The paragraphs in this range do not need to begin on a new page.</td>
</tr>
<tr>
<td>tomUndefined</td>
<td>The property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetPageBreakBefore</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/6f94aba1-62df-4714-ab50-a86fc679f407">SetPageBreakBefore</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

