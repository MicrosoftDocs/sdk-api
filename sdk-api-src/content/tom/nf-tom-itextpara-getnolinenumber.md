---
UID: NF:tom.ITextPara.GetNoLineNumber
title: ITextPara::GetNoLineNumber
author: windows-sdk-content
description: Determines whether paragraph numbering is enabled.
old-location: controls\ITextPara_GetNoLineNumber.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getnolinenumber.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetNoLineNumber, GetNoLineNumber method [Windows Controls], GetNoLineNumber method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetNoLineNumber method, ITextPara.GetNoLineNumber, ITextPara::GetNoLineNumber, _win32_ITextPara_GetNoLineNumber, _win32_ITextPara_GetNoLineNumber_cpp, controls.ITextPara_GetNoLineNumber, controls._win32_ITextPara_GetNoLineNumber, tom/ITextPara::GetNoLineNumber
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
 - ITextPara.GetNoLineNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetNoLineNumber


## -description


Determines whether paragraph numbering is enabled.


## -parameters




### -param pValue

TBD




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
<td>Line numbering is disabled.</td>
</tr>
<tr>
<td>tomFalse</td>
<td>Line numbering is enabled.</td>
</tr>
<tr>
<td>tomUndefined</td>
<td>The property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetNoLineNumber</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
 




## -remarks



Paragraph numbering is when the paragraphs of a range are numbered. The number appears on the first line of a paragraph.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/d4c8d079-f832-4030-98eb-4a07cb7a8f05">SetNoLineNumber</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

