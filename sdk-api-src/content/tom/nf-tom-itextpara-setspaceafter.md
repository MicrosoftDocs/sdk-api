---
UID: NF:tom.ITextPara.SetSpaceAfter
title: ITextPara::SetSpaceAfter (tom.h)
description: Sets the amount of space that follows a paragraph.helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetSpaceAfter method","ITextPara.SetSpaceAfter","ITextPara::SetSpaceAfter","SetSpaceAfter","SetSpaceAfter method [Windows Controls]","SetSpaceAfter method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetSpaceAfter","_win32_ITextPara_SetSpaceAfter_cpp","controls.ITextPara_SetSpaceAfter","controls._win32_ITextPara_SetSpaceAfter","tom/ITextPara::SetSpaceAfter"]
old-location: controls\ITextPara_SetSpaceAfter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setspaceafter.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetSpaceAfter method, ITextPara.SetSpaceAfter, ITextPara::SetSpaceAfter, SetSpaceAfter, SetSpaceAfter method [Windows Controls], SetSpaceAfter method [Windows Controls],ITextPara interface, _win32_ITextPara_SetSpaceAfter, _win32_ITextPara_SetSpaceAfter_cpp, controls.ITextPara_SetSpaceAfter, controls._win32_ITextPara_SetSpaceAfter, tom/ITextPara::SetSpaceAfter
f1_keywords:
- tom/ITextPara.SetSpaceAfter
dev_langs:
- c++
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
- ITextPara.SetSpaceAfter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara::SetSpaceAfter


## -description


Sets the amount of space that follows a paragraph.


## -parameters




### -param Value [in]

Type: <b>float</b>

New space-after value, in floating-point points. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::SetSpaceAfter</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
 

 

