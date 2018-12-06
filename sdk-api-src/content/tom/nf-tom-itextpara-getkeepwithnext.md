---
UID: NF:tom.ITextPara.GetKeepWithNext
title: ITextPara::GetKeepWithNext
author: windows-sdk-content
description: Determines whether page breaks are allowed between paragraphs in the range.
old-location: controls\ITextPara_GetKeepWithNext.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getkeepwithnext.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKeepWithNext, GetKeepWithNext method [Windows Controls], GetKeepWithNext method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetKeepWithNext method, ITextPara.GetKeepWithNext, ITextPara::GetKeepWithNext, _win32_ITextPara_GetKeepWithNext, _win32_ITextPara_GetKeepWithNext_cpp, controls.ITextPara_GetKeepWithNext, controls._win32_ITextPara_GetKeepWithNext, tom/ITextPara::GetKeepWithNext, tomFalse, tomTrue, tomUndefined
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
 - ITextPara.GetKeepWithNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetKeepWithNext


## -description


Determines whether page breaks are allowed between paragraphs in the range.


## -parameters




### -param pValue

Type: <b>long*</b>

A variable that is one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomTrue"></a><a id="tomtrue"></a><a id="TOMTRUE"></a><dl>
<dt><b>tomTrue</b></dt>
</dl>
</td>
<td width="60%">
Page breaks are not allowed between paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="tomFalse"></a><a id="tomfalse"></a><a id="TOMFALSE"></a><dl>
<dt><b>tomFalse</b></dt>
</dl>
</td>
<td width="60%">
Page breaks are allowed between paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUndefined"></a><a id="tomundefined"></a><a id="TOMUNDEFINED"></a><dl>
<dt><b>tomUndefined</b></dt>
</dl>
</td>
<td width="60%">
The property is undefined.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetKeepWithNext</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



This property corresponds to the PFE_KEEPNEXT effect described in the <a href="https://msdn.microsoft.com/96c8ec3e-3d4c-4233-993b-201f4c62e653">PARAFORMAT2</a> structure. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<a href="https://msdn.microsoft.com/96c8ec3e-3d4c-4233-993b-201f4c62e653">PARAFORMAT2</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/cc90c377-bae6-4aa8-8bb8-26dc9c915bae">SetKeepWithNext</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

