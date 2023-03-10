---
UID: NF:tom.ITextDocument2.GetEffectColor
title: ITextDocument2::GetEffectColor (tom.h)
description: Retrieves the color used for special text attributes.
helpviewer_keywords: ["GetEffectColor","GetEffectColor method [Windows Controls]","GetEffectColor method [Windows Controls]","ITextDocument2 interface","ITextDocument2 interface [Windows Controls]","GetEffectColor method","ITextDocument2.GetEffectColor","ITextDocument2::GetEffectColor","controls.itextdocument2_geteffectcolor","tom/ITextDocument2::GetEffectColor"]
old-location: controls\itextdocument2_geteffectcolor.htm
tech.root: Controls
ms.assetid: 4bc2740e-852f-430b-913e-5d28baec3272
ms.date: 12/05/2018
ms.keywords: GetEffectColor, GetEffectColor method [Windows Controls], GetEffectColor method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetEffectColor method, ITextDocument2.GetEffectColor, ITextDocument2::GetEffectColor, controls.itextdocument2_geteffectcolor, tom/ITextDocument2::GetEffectColor
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextDocument2::GetEffectColor
 - tom/ITextDocument2::GetEffectColor
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
 - ITextDocument2.GetEffectColor
---

# ITextDocument2::GetEffectColor


## -description

Retrieves the color used for special text attributes.

## -parameters

### -param Index [in]

Type: <b>long</b>

The index of the color to retrieve. It can be one of the following values.

<table>
<tr>
<th>Index</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Text color.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
RGB(0, 255, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
RGB(0, 255,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
RGB(255,   0, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
RGB(255,   0, 0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
RGB(255,   255, 0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
RGB(255,   255, 255)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9</dt>
</dl>
</td>
<td width="60%">
RGB(0,   0, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
RGB(0,   128, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
RGB(0, 128,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>12</dt>
</dl>
</td>
<td width="60%">
RGB(128,   0, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>13</dt>
</dl>
</td>
<td width="60%">
RGB(128,   0,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>14</dt>
</dl>
</td>
<td width="60%">
RGB(128, 128,   0)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>15</dt>
</dl>
</td>
<td width="60%">
RGB(128, 128, 128)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16</dt>
</dl>
</td>
<td width="60%">
RGB(192, 192, 192)

</td>
</tr>
</table>

### -param pValue [out]

Type: <b>long*</b>

The color that corresponds to the specified index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The first 16 index values are for special underline colors. If an index between 1 and 16 hasn't been defined by a call to the <a href="/windows/desktop/api/tom/nf-tom-itextdocument2-seteffectcolor">ITextDocument2:SetEffectColor</a> method, <b>GetEffectColor</b> returns the corresponding Microsoft Word default color.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextdocument2">ITextDocument2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument2-seteffectcolor">ITextDocument2::SetEffectColor</a>