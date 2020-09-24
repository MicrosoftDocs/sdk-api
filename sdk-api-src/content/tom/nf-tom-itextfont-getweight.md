---
UID: NF:tom.ITextFont.GetWeight
title: ITextFont::GetWeight (tom.h)
description: Gets the font weight for the characters in a range.
helpviewer_keywords: ["GetWeight","GetWeight method [Windows Controls]","GetWeight method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetWeight method","ITextFont.GetWeight","ITextFont::GetWeight","_win32_ITextFont_GetWeight","_win32_ITextFont_GetWeight_cpp","controls.ITextFont_GetWeight","controls._win32_ITextFont_GetWeight","tom/ITextFont::GetWeight"]
old-location: controls\ITextFont_GetWeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getweight.htm
ms.date: 12/05/2018
ms.keywords: GetWeight, GetWeight method [Windows Controls], GetWeight method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetWeight method, ITextFont.GetWeight, ITextFont::GetWeight, _win32_ITextFont_GetWeight, _win32_ITextFont_GetWeight_cpp, controls.ITextFont_GetWeight, controls._win32_ITextFont_GetWeight, tom/ITextFont::GetWeight
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont::GetWeight
 - tom/ITextFont::GetWeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont.GetWeight
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
				<a href="/windows/desktop/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> structure and the 
				<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a> interface. Windows defines the following degrees of font weight. 

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

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setweight">SetWeight</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>