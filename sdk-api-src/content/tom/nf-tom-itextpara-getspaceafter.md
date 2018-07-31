---
UID: NF:tom.ITextPara.GetSpaceAfter
title: ITextPara::GetSpaceAfter
author: windows-sdk-content
description: Retrieves the amount of vertical space below a paragraph.
old-location: controls\ITextPara_GetSpaceAfter.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getspaceafter.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetSpaceAfter, GetSpaceAfter method [Windows Controls], GetSpaceAfter method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetSpaceAfter method, ITextPara.GetSpaceAfter, ITextPara::GetSpaceAfter, _win32_ITextPara_GetSpaceAfter, _win32_ITextPara_GetSpaceAfter_cpp, controls.ITextPara_GetSpaceAfter, controls._win32_ITextPara_GetSpaceAfter, tom/ITextPara::GetSpaceAfter
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
 - ITextPara.GetSpaceAfter
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetSpaceAfter


## -description


Retrieves the amount of vertical space below a paragraph. 


## -parameters




### -param pValue

Type: <b>float*</b>

The space-after value, in floating-point points. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetSpaceAfter</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



<a href="https://msdn.microsoft.com/86c453b5-e839-42d6-9ef8-d2c1c0f54af3">GetSpaceBefore</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3e4fb12e-a7ac-4776-be66-ad5e4fdf9370">SetSpaceAfter</a>



<a href="https://msdn.microsoft.com/003aa8d2-f80e-4925-8e25-dcb3ea6d95cf">SetSpaceBefore</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

