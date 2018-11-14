---
UID: NF:tom.ITextFont.GetEngrave
title: ITextFont::GetEngrave
author: windows-sdk-content
description: Gets whether characters are displayed as imprinted characters.
old-location: controls\ITextFont_GetEngrave.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getengrave.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetEngrave, GetEngrave method [Windows Controls], GetEngrave method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetEngrave method, ITextFont.GetEngrave, ITextFont::GetEngrave, _win32_ITextFont_GetEngrave, _win32_ITextFont_GetEngrave_cpp, controls.ITextFont_GetEngrave, controls._win32_ITextFont_GetEngrave, tom/ITextFont::GetEngrave
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
 - ITextFont.GetEngrave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextFont.GetEngrave
: 
---

# ITextFont::GetEngrave


## -description


Gets whether characters are displayed as imprinted characters.


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
<td>Characters are displayed as imprinted characters.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not displayed as imprinted characters.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The Engrave property is undefined.</td>
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



This property corresponds to the <b>CFE_IMPRINT</b> effect described in the <a href="https://msdn.microsoft.com/e0057d40-e479-4706-b677-b8fb727a8118">CHARFORMAT2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/e0057d40-e479-4706-b677-b8fb727a8118">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/dbc2b175-e0bb-4d10-87ad-b8c07cadab5c">SetEngrave</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

