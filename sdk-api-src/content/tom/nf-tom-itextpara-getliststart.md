---
UID: NF:tom.ITextPara.GetListStart
title: ITextPara::GetListStart method
author: windows-driver-content
description: Retrieves the starting value or code of a list numbering sequence.
old-location: controls\ITextPara_GetListStart.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getliststart.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetListStart method [Windows Controls], GetListStart method [Windows Controls], ITextPara interface, GetListStart,ITextPara.GetListStart, ITextPara, ITextPara interface [Windows Controls], GetListStart method, ITextPara::GetListStart, _win32_ITextPara_GetListStart, _win32_ITextPara_GetListStart_cpp, controls.ITextPara_GetListStart, controls._win32_ITextPara_GetListStart, tom/ITextPara::GetListStart
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
-	ITextPara.GetListStart
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetListStart method


## -description


Retrieves the starting value or code of a list numbering sequence. 


## -parameters




### -param pValue

Type: <b>long*</b>

The starting value or code of a list numbering sequence. For the possible values, see the <a href="https://msdn.microsoft.com/df2b0821-9216-465a-b066-60807a0b3e0f">ITextPara::GetListType</a> method. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetListStart</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



For a discussion on which sequence to use, see the <a href="https://msdn.microsoft.com/df2b0821-9216-465a-b066-60807a0b3e0f">ITextPara::GetListType</a> method.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/df2b0821-9216-465a-b066-60807a0b3e0f">GetListType</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1ba2346a-b56a-4eda-a6f9-0563e71c9cbd">SetListStart</a>



<a href="https://msdn.microsoft.com/5f9adb67-e4d6-41c9-b360-efbcead7befc">SetListType</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

