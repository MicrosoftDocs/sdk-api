---
UID: NF:tom.ITextFont.SetEmboss
title: ITextFont::SetEmboss
author: windows-sdk-content
description: Sets whether characters are embossed.
old-location: controls\ITextFont_SetEmboss.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setemboss.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextFont interface [Windows Controls],SetEmboss method, ITextFont.SetEmboss, ITextFont::SetEmboss, SetEmboss, SetEmboss method [Windows Controls], SetEmboss method [Windows Controls],ITextFont interface, _win32_ITextFont_SetEmboss, _win32_ITextFont_SetEmboss_cpp, controls.ITextFont_SetEmboss, controls._win32_ITextFont_SetEmboss, tom/ITextFont::SetEmboss
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
 - ITextFont.SetEmboss
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::SetEmboss


## -description


Sets whether characters are embossed.


## -parameters




### -param Value [in]

Type: <b>long</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are embossed.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not embossed.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the state of the Emboss property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Emboss property is undefined.</td>
</tr>
</table>
 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
The font object is attached to a range that has been deleted.

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
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/eeb1d10d-c326-4052-813b-ee435b88e835">GetEmboss</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

