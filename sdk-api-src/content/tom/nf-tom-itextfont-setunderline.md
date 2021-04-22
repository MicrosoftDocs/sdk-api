---
UID: NF:tom.ITextFont.SetUnderline
title: ITextFont::SetUnderline (tom.h)
description: Sets the type of underlining for the characters in a range.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","SetUnderline method","ITextFont.SetUnderline","ITextFont::SetUnderline","SetUnderline","SetUnderline method [Windows Controls]","SetUnderline method [Windows Controls]","ITextFont interface","_win32_ITextFont_SetUnderline","_win32_ITextFont_SetUnderline_cpp","controls.ITextFont_SetUnderline","controls._win32_ITextFont_SetUnderline","tom/ITextFont::SetUnderline","tomDash","tomDashDot","tomDashDotDot","tomDotted","tomDouble","tomDoubleWave","tomHair","tomHeavyWave","tomLongDash","tomNone","tomSingle","tomThick","tomThickDash","tomThickDashDot","tomThickDashDotDot","tomThickDotted","tomThickLongDash","tomWave","tomWords"]
old-location: controls\ITextFont_SetUnderline.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setunderline.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],SetUnderline method, ITextFont.SetUnderline, ITextFont::SetUnderline, SetUnderline, SetUnderline method [Windows Controls], SetUnderline method [Windows Controls],ITextFont interface, _win32_ITextFont_SetUnderline, _win32_ITextFont_SetUnderline_cpp, controls.ITextFont_SetUnderline, controls._win32_ITextFont_SetUnderline, tom/ITextFont::SetUnderline, tomDash, tomDashDot, tomDashDotDot, tomDotted, tomDouble, tomDoubleWave, tomHair, tomHeavyWave, tomLongDash, tomNone, tomSingle, tomThick, tomThickDash, tomThickDashDot, tomThickDashDotDot, tomThickDotted, tomThickLongDash, tomWave, tomWords
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
 - ITextFont::SetUnderline
 - tom/ITextFont::SetUnderline
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
 - ITextFont.SetUnderline
---

# ITextFont::SetUnderline


## -description

Sets thevtype of underlining for the characters in a range.

## -parameters

### -param Value [in]

Type: <b>long</b>

The type of underlining. It can be one of the following values.

<a id="tomNone"></a>
<a id="tomnone"></a>
<a id="TOMNONE"></a>


#### tomNone

<a id="tomSingle"></a>
<a id="tomsingle"></a>
<a id="TOMSINGLE"></a>


#### tomSingle

<a id="tomWords"></a>
<a id="tomwords"></a>
<a id="TOMWORDS"></a>


#### tomWords

<a id="tomDouble"></a>
<a id="tomdouble"></a>
<a id="TOMDOUBLE"></a>


#### tomDouble

<a id="tomDotted"></a>
<a id="tomdotted"></a>
<a id="TOMDOTTED"></a>


#### tomDotted

<a id="tomDash"></a>
<a id="tomdash"></a>
<a id="TOMDASH"></a>


#### tomDash

<a id="tomDashDot"></a>
<a id="tomdashdot"></a>
<a id="TOMDASHDOT"></a>


#### tomDashDot

<a id="tomDashDotDot"></a>
<a id="tomdashdotdot"></a>
<a id="TOMDASHDOTDOT"></a>


#### tomDashDotDot

<a id="tomWave"></a>
<a id="tomwave"></a>
<a id="TOMWAVE"></a>


#### tomWave

<a id="tomThick"></a>
<a id="tomthick"></a>
<a id="TOMTHICK"></a>


#### tomThick

<a id="tomHair"></a>
<a id="tomhair"></a>
<a id="TOMHAIR"></a>


#### tomHair

<a id="tomDoubleWave"></a>
<a id="tomdoublewave"></a>
<a id="TOMDOUBLEWAVE"></a>


#### tomDoubleWave

<a id="tomHeavyWave"></a>
<a id="tomheavywave"></a>
<a id="TOMHEAVYWAVE"></a>


#### tomHeavyWave

<a id="tomLongDash"></a>
<a id="tomlongdash"></a>
<a id="TOMLONGDASH"></a>


#### tomLongDash

<a id="tomThickDash"></a>
<a id="tomthickdash"></a>
<a id="TOMTHICKDASH"></a>


#### tomThickDash

<a id="tomThickDashDot"></a>
<a id="tomthickdashdot"></a>
<a id="TOMTHICKDASHDOT"></a>


#### tomThickDashDot

<a id="tomThickDashDotDot"></a>
<a id="tomthickdashdotdot"></a>
<a id="TOMTHICKDASHDOTDOT"></a>


#### tomThickDashDotDot

<a id="tomThickDotted"></a>
<a id="tomthickdotted"></a>
<a id="TOMTHICKDOTTED"></a>


#### tomThickDotted

<a id="tomThickLongDash"></a>
<a id="tomthicklongdash"></a>
<a id="TOMTHICKLONGDASH"></a>


#### tomThickLongDash

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getunderline">GetUnderline</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>