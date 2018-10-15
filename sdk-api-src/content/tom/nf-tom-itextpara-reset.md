---
UID: NF:tom.ITextPara.Reset
title: ITextPara::Reset
author: windows-sdk-content
description: Resets the paragraph formatting to a choice of default values.
old-location: controls\ITextPara_Reset.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparareset.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ITextPara interface [Windows Controls],Reset method, ITextPara.Reset, ITextPara::Reset, Reset, Reset method [Windows Controls], Reset method [Windows Controls],ITextPara interface, _win32_ITextPara_Reset, _win32_ITextPara_Reset_cpp, controls.ITextPara_Reset, controls._win32_ITextPara_Reset, tom/ITextPara::Reset
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
 - ITextPara.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara::Reset


## -description


Resets the paragraph formatting to a choice of default values. 


## -parameters




### -param Value [in]

Type: <b>long</b>

Type of reset. It can be one of the following possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt><a href="tomconstants.htm">tomDefault</a></dt>
</dl>
</td>
<td width="60%">
Used for paragraph formatting that is defined by the RTF \pard, that is, the paragraph default control word.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt><a href="tomconstants.htm">tomUndefined</a></dt>
</dl>
</td>
<td width="60%">
Used for all undefined values. The tomUndefined value is only valid for duplicate (clone) <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> objects.

</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::Reset</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

