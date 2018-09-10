---
UID: NF:tom.ITextPara.GetListLevelIndex
title: ITextPara::GetListLevelIndex
author: windows-sdk-content
description: Retrieves the list level index used with paragraphs.
old-location: controls\ITextPara_GetListLevelIndex.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlistlevelindex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetListLevelIndex, GetListLevelIndex method [Windows Controls], GetListLevelIndex method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetListLevelIndex method, ITextPara.GetListLevelIndex, ITextPara::GetListLevelIndex, _win32_ITextPara_GetListLevelIndex, _win32_ITextPara_GetListLevelIndex_cpp, controls.ITextPara_GetListLevelIndex, controls._win32_ITextPara_GetListLevelIndex, tom/ITextPara::GetListLevelIndex
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
 - ITextPara.GetListLevelIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetListLevelIndex


## -description


Retrieves the list level index used with paragraphs.


## -parameters




### -param pValue

Type: <b>long*</b>

A variable that is the list level index. The value of <i>pValue</i> can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>No list.</td>
</tr>
<tr>
<td>1</td>
<td>First-level (outermost) list.</td>
</tr>
<tr>
<td>2</td>
<td>Second-level (nested) list. This is nested under a level 1 list item.</td>
</tr>
<tr>
<td>3</td>
<td>Third-level (nested) list. This is nested under a level 2 list item.</td>
</tr>
<tr>
<td>and so forth</td>
<td>Nesting continues similarly.</td>
</tr>
</table>
 

Up to three levels are common in HTML documents. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetListLevelIndex</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



<a href="https://msdn.microsoft.com/en-us/library/Bb774173(v=VS.85).aspx">SetListLevelIndex</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

