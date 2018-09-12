---
UID: NF:tom.ITextRange.Cut
title: ITextRange::Cut
author: windows-sdk-content
description: Cuts the plain or rich text to a data object or to the Clipboard, depending on the pVar parameter.
old-location: controls\ITextRange_Cut.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\cut.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Cut, Cut method [Windows Controls], Cut method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Cut method, ITextRange.Cut, ITextRange::Cut, _win32_ITextRange_Cut, _win32_ITextRange_Cut_cpp, controls.ITextRange_Cut, controls._win32_ITextRange_Cut, tom/ITextRange::Cut
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
 - ITextRange.Cut
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::Cut


## -description


Cuts the plain or rich text to a data object or to the Clipboard, depending on the 
			<i>pVar</i> parameter. 


## -parameters




### -param pVar

Type: <b>VARIANT*</b>

The cut text. 
					<i>pVar</i>-&gt;ppunkVal is the out parameter for an 
					<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> object, provided that the following conditions exist: 
				

<ul>
<li>pVar-&gt;vt = (VT_UNKNOWN | VT_BYREF) </li>
<li>pVar is not null </li>
<li>pVar-&gt;ppunkVal is not null </li>
</ul>
Otherwise, the clipboard is used. 


## -returns



Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise it returns one of the following values. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

