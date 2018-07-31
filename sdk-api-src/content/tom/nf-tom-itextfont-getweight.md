---
UID: NF:tom.ITextFont.GetWeight
title: ITextFont::GetWeight
author: windows-sdk-content
description: Gets the font weight for the characters in a range.
old-location: controls\ITextFont_GetWeight.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getweight.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetWeight, GetWeight method [Windows Controls], GetWeight method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetWeight method, ITextFont.GetWeight, ITextFont::GetWeight, _win32_ITextFont_GetWeight, _win32_ITextFont_GetWeight_cpp, controls.ITextFont_GetWeight, controls._win32_ITextFont_GetWeight, tom/ITextFont::GetWeight
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
 - ITextFont.GetWeight
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont::GetWeight


## -description


Gets the font weight for the characters in a range.


## -parameters




### -param pValue

Type: <b>long*</b>

The font weight. The
				Bold property is a binary version of the 
				Weight property that sets the weight to <b>FW_BOLD</b>. The font weight exists in the 
				<a href="https://msdn.microsoft.com/57658a03-0a6d-4a28-a7c1-c65ec145beb4">LOGFONT</a> structure and the 
				<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a> interface. Windows defines the following degrees of font weight. 

<table class="clsStd">
<tr>
<th>Font weight</th>
<th>Value</th>
</tr>
<tr>
<td><b>FW_DONTCARE</b></td>
<td>0</td>
</tr>
<tr>
<td><b>FW_THIN</b></td>
<td>100</td>
</tr>
<tr>
<td><b>FW_EXTRALIGHT</b></td>
<td>200</td>
</tr>
<tr>
<td><b>FW_LIGHT</b></td>
<td>300</td>
</tr>
<tr>
<td><b>FW_NORMAL</b></td>
<td>400</td>
</tr>
<tr>
<td><b>FW_MEDIUM</b></td>
<td>500</td>
</tr>
<tr>
<td><b>FW_SEMIBOLD</b></td>
<td>600</td>
</tr>
<tr>
<td><b>FW_BOLD</b></td>
<td>700</td>
</tr>
<tr>
<td><b>FW_EXTRABOLD</b></td>
<td>800</td>
</tr>
<tr>
<td><b>FW_HEAVY</b></td>
<td>900</td>
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
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/12ca699b-8e9c-4071-aac9-783480541526">SetWeight</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

