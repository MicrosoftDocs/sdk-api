---
UID: NF:tom.ITextFont.GetBold
title: ITextFont::GetBold
author: windows-sdk-content
description: Gets whether the characters are bold.
old-location: controls\ITextFont_GetBold.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getbold.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetBold, GetBold method [Windows Controls], GetBold method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetBold method, ITextFont.GetBold, ITextFont::GetBold, _win32_ITextFont_GetBold, _win32_ITextFont_GetBold_cpp, controls.ITextFont_GetBold, controls._win32_ITextFont_GetBold, tom/ITextFont::GetBold
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
 - ITextFont.GetBold
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetBold


## -description


Gets whether the characters are bold.


## -parameters




### -param pValue

Type: <b>long*</b>

A <a href="About_Text_Object_Model.htm">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are bold.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not bold.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Bold property is undefined.</td>
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
</table>
 




## -remarks



You can use the <a href="https://msdn.microsoft.com/12ca699b-8e9c-4071-aac9-783480541526">ITextFont::SetWeight</a> and <a href="https://msdn.microsoft.com/6bbbcd2d-3d40-4c87-a786-13acbf2be502">ITextFont::GetWeight</a> methods to set or retrieve the font weight more precisely than the <a href="https://msdn.microsoft.com/3e2bcd5a-badd-4ba4-8d8b-d054ec4ac539">ITextFont::SetBold</a>and <b>ITextFont::GetBold</b> methods.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6bbbcd2d-3d40-4c87-a786-13acbf2be502">GetWeight</a>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3e2bcd5a-badd-4ba4-8d8b-d054ec4ac539">SetBold</a>



<a href="https://msdn.microsoft.com/12ca699b-8e9c-4071-aac9-783480541526">SetWeight</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

