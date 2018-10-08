---
UID: NF:tom.ITextPara.GetWidowControl
title: ITextPara::GetWidowControl
author: windows-sdk-content
description: Retrieves the widow and orphan control state for the paragraphs in a range.
old-location: controls\ITextPara_GetWidowControl.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getwidowcontrol.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetWidowControl, GetWidowControl method [Windows Controls], GetWidowControl method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetWidowControl method, ITextPara.GetWidowControl, ITextPara::GetWidowControl, _win32_ITextPara_GetWidowControl, _win32_ITextPara_GetWidowControl_cpp, controls.ITextPara_GetWidowControl, controls._win32_ITextPara_GetWidowControl, tom/ITextPara::GetWidowControl
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
 - ITextPara.GetWidowControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::GetWidowControl


## -description


Retrieves the widow and orphan control state for the paragraphs in a range.


## -parameters




### -param pValue

TBD




#### - pBool

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that indicates the state of widow and orphan control. It can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Prevents the printing of a widow or orphan</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Allows the printing of a widow or orphan.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The widow-control property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetWidowControl</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



A widow is created when the last line of a paragraph is printed by itself at the top of a page. An orphan is when the first line of a paragraph is printed by itself at the bottom of a page.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787834(v=VS.85).aspx">SetWidowControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

