---
UID: NF:tom.ITextRange.SetPara
title: ITextRange::SetPara
author: windows-sdk-content
description: Sets the paragraph attributes of this range to those of the specified ITextPara object.
old-location: controls\ITextRange_SetPara.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setpara.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextRange interface [Windows Controls],SetPara method, ITextRange.SetPara, ITextRange::SetPara, SetPara, SetPara method [Windows Controls], SetPara method [Windows Controls],ITextRange interface, _win32_ITextRange_SetPara, _win32_ITextRange_SetPara_cpp, controls.ITextRange_SetPara, controls._win32_ITextRange_SetPara, tom/ITextRange::SetPara
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
 - ITextRange.SetPara
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::SetPara


## -description


Sets the paragraph attributes of this range to those of the specified <a href="https://msdn.microsoft.com/library/Bb774056(v=VS.85).aspx">ITextPara</a> object.


## -parameters




### -param pPara [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb774056(v=VS.85).aspx">ITextPara</a>*</b>

The paragraph object with the desired paragraph format. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPara</i> is null.

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



<a href="https://msdn.microsoft.com/library/Bb774001(v=VS.85).aspx">GetPara</a>



<a href="https://msdn.microsoft.com/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

