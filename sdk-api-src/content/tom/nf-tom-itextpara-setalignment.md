---
UID: NF:tom.ITextPara.SetAlignment
title: ITextPara::SetAlignment method
author: windows-driver-content
description: Sets the paragraph alignment.
old-location: controls\ITextPara_SetAlignment.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setalignment.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextPara, ITextPara interface [Windows Controls], SetAlignment method, ITextPara::SetAlignment, SetAlignment method [Windows Controls], SetAlignment method [Windows Controls], ITextPara interface, SetAlignment,ITextPara.SetAlignment, _win32_ITextPara_SetAlignment, _win32_ITextPara_SetAlignment_cpp, controls.ITextPara_SetAlignment, controls._win32_ITextPara_SetAlignment, tom/ITextPara::SetAlignment
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextPara.SetAlignment
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::SetAlignment method


## -description


Sets the paragraph alignment. 


## -parameters




### -param Value [in]

Type: <b>long</b>

New paragraph alignment. For a list of possible values, see the <a href="https://msdn.microsoft.com/d97c5efb-3007-40f5-b4f5-30a3505e01aa">ITextPara::GetAlignment</a> method. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::SetAlignment</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



<a href="https://msdn.microsoft.com/d97c5efb-3007-40f5-b4f5-30a3505e01aa">GetAlignment</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

