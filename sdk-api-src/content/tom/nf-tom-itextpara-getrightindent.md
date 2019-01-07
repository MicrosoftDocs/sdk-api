---
UID: NF:tom.ITextPara.GetRightIndent
title: ITextPara::GetRightIndent
author: windows-sdk-content
description: Retrieves the size of the right margin indent of a paragraph.
old-location: controls\ITextPara_GetRightIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getrightindent.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRightIndent, GetRightIndent method [Windows Controls], GetRightIndent method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetRightIndent method, ITextPara.GetRightIndent, ITextPara::GetRightIndent, _win32_ITextPara_GetRightIndent, _win32_ITextPara_GetRightIndent_cpp, controls.ITextPara_GetRightIndent, controls._win32_ITextPara_GetRightIndent, tom/ITextPara::GetRightIndent
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
 - ITextPara.GetRightIndent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetRightIndent


## -description


Retrieves the size of the right margin indent of a paragraph. 


## -parameters




### -param pValue

Type: <b>float*</b>

The right indentation, in floating-point points. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetRightIndent</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



<a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787807(v=VS.85).aspx">SetRightIndent</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

