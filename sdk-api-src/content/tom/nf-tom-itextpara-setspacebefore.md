---
UID: NF:tom.ITextPara.SetSpaceBefore
title: ITextPara::SetSpaceBefore (tom.h)
author: windows-sdk-content
description: Sets the amount of space preceding a paragraph.
old-location: controls\ITextPara_SetSpaceBefore.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setspacebefore.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetSpaceBefore method, ITextPara.SetSpaceBefore, ITextPara::SetSpaceBefore, SetSpaceBefore, SetSpaceBefore method [Windows Controls], SetSpaceBefore method [Windows Controls],ITextPara interface, _win32_ITextPara_SetSpaceBefore, _win32_ITextPara_SetSpaceBefore_cpp, controls.ITextPara_SetSpaceBefore, controls._win32_ITextPara_SetSpaceBefore, tom/ITextPara::SetSpaceBefore
ms.topic: method
f1_keywords: 
 - "tom/ITextPara.SetSpaceBefore"
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
 - ITextPara.SetSpaceBefore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara::SetSpaceBefore


## -description


Sets the amount of space preceding a paragraph.


## -parameters




### -param Value [in]

Type: <b>float</b>

New space-before value, in floating-point points. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::SetSpaceBefore</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

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



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

