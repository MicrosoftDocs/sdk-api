---
UID: NF:tom.ITextFont.GetSmallCaps
title: ITextFont::GetSmallCaps
author: windows-sdk-content
description: Gets whether characters are in small capital letters.
old-location: controls\ITextFont_GetSmallCaps.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getsmallcaps.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetSmallCaps, GetSmallCaps method [Windows Controls], GetSmallCaps method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetSmallCaps method, ITextFont.GetSmallCaps, ITextFont::GetSmallCaps, _win32_ITextFont_GetSmallCaps, _win32_ITextFont_GetSmallCaps_cpp, controls.ITextFont_GetSmallCaps, controls._win32_ITextFont_GetSmallCaps, tom/ITextFont::GetSmallCaps
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
 - ITextFont.GetSmallCaps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont::GetSmallCaps


## -description


Gets whether characters are in small capital letters.


## -parameters




### -param pValue

Type: <b>long*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">tomBool</a> value that can be one of the following.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Characters are in small capital letters.</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Characters are not in small capital letters.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The SmallCaps property is undefined.</td>
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



This property corresponds to the <b>CFE_SMALLCAPS</b> effect described in the <a href="https://msdn.microsoft.com/en-us/library/Bb787883(v=VS.85).aspx">CHARFORMAT2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787883(v=VS.85).aspx">CHARFORMAT2</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787815(v=VS.85).aspx">SetSmallCaps</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

