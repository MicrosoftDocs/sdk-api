---
UID: NF:tom.ITextFont.SetOutline
title: ITextFont::SetOutline
author: windows-sdk-content
description: Sets whether characters are displayed as outlined characters.
old-location: controls\ITextFont_SetOutline.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setoutline.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextFont interface [Windows Controls],SetOutline method, ITextFont.SetOutline, ITextFont::SetOutline, SetOutline, SetOutline method [Windows Controls], SetOutline method [Windows Controls],ITextFont interface, _win32_ITextFont_SetOutline, _win32_ITextFont_SetOutline_cpp, controls.ITextFont_SetOutline, controls._win32_ITextFont_SetOutline, tom/ITextFont::SetOutline
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
 - ITextFont.SetOutline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::SetOutline


## -description


Sets whether characters are displayed as outlined characters.


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
<td>Characters are outlined.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not outlined.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the state of the Outline property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Outline property is undefined.</td>
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



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1e080903-0a3d-4686-83ab-b50864354347">SetOutline</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

