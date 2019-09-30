---
UID: NF:tom.ITextPara.SetDuplicate
title: ITextPara::SetDuplicate (tom.h)
author: windows-sdk-content
description: Sets the formatting for an existing paragraph by copying a given format.
old-location: controls\ITextPara_SetDuplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparasetduplicate.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetDuplicate method, ITextPara.SetDuplicate, ITextPara::SetDuplicate, SetDuplicate, SetDuplicate method [Windows Controls], SetDuplicate method [Windows Controls],ITextPara interface, _win32_ITextPara_SetDuplicate, _win32_ITextPara_SetDuplicate_cpp, controls.ITextPara_SetDuplicate, controls._win32_ITextPara_SetDuplicate, tom/ITextPara::SetDuplicate
ms.topic: method
f1_keywords: 
 - "tom/ITextPara.SetDuplicate"
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
 - ITextPara.SetDuplicate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara::SetDuplicate


## -description


Sets the formatting for an existing paragraph by copying a given format. 


## -parameters




### -param pPara [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> range that contains the new paragraph formatting. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::SetDuplicate</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
 




## -remarks



The tomUndefined values have no effect, that is, they will not change the target values.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>
 

 

