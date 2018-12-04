---
UID: NF:tom.ITextFont.SetProtected
title: ITextFont::SetProtected
author: windows-sdk-content
description: Sets whether characters are protected against attempts to modify them.
old-location: controls\ITextFont_SetProtected.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setprotected.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ITextFont interface [Windows Controls],SetProtected method, ITextFont.SetProtected, ITextFont::SetProtected, SetProtected, SetProtected method [Windows Controls], SetProtected method [Windows Controls],ITextFont interface, _win32_ITextFont_SetProtected, _win32_ITextFont_SetProtected_cpp, controls.ITextFont_SetProtected, controls._win32_ITextFont_SetProtected, tom/ITextFont::SetProtected
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
 - ITextFont.SetProtected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::SetProtected


## -description


Sets whether characters are protected against attempts to modify them.


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
<td>Characters are protected.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not protected.</td>
</tr>
<tr>
<td><b>tomToggle</b></td>
<td>Toggle the state of the Protected property.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Protected property is undefined.</td>
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
 




## -remarks



In general, Text Object Model (TOM) methods that attempt to change the formatting or content of a range will fail with <b>E_ACCESSDENIED</b> if any part of that range is protected or if the document is read-only. To make a change in protected text, the TOM client should attempt to turn off the protection of the text to be modified. The owner of the document may permit this to happen. For example in rich edit controls, attempts to change protected text result in an <a href="https://msdn.microsoft.com/29c0cb51-675c-44b1-ad45-5f7140ca5675">EN_PROTECTED</a> notification code to the creator of the document, who then can refuse or grant permission for the change. The creator is the client that created a windowed rich-edit control through the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> function or the <a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a> object that called the <a href="https://msdn.microsoft.com/475ede7d-75ba-4eda-8253-1166fc9f45fe">CreateTextServices</a> function to create a windowless rich edit control.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/475ede7d-75ba-4eda-8253-1166fc9f45fe">CreateTextServices</a>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/29c0cb51-675c-44b1-ad45-5f7140ca5675">EN_PROTECTED</a>



<a href="https://msdn.microsoft.com/c0696172-e6c2-4b26-9bb3-e58d31100e5b">GetProtected</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

