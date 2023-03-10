---
UID: NF:tom.ITextFont.Reset
title: ITextFont::Reset (tom.h)
description: Resets the character formatting to the specified values.
helpviewer_keywords: ["ITextFont interface [Windows Controls]","Reset method","ITextFont.Reset","ITextFont::Reset","Reset","Reset method [Windows Controls]","Reset method [Windows Controls]","ITextFont interface","_win32_ITextFont_Reset","_win32_ITextFont_Reset_cpp","controls.ITextFont_Reset","controls._win32_ITextFont_Reset","tom/ITextFont::Reset","tomApplyLater","tomApplyNow","tomApplyTmp","tomCacheParms","tomDefault","tomDisableSmartFont","tomEnableSmartFont","tomTrackParms","tomUndefined","tomUsePoints","tomUseTwips"]
old-location: controls\ITextFont_Reset.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontreset.htm
ms.date: 12/05/2018
ms.keywords: ITextFont interface [Windows Controls],Reset method, ITextFont.Reset, ITextFont::Reset, Reset, Reset method [Windows Controls], Reset method [Windows Controls],ITextFont interface, _win32_ITextFont_Reset, _win32_ITextFont_Reset_cpp, controls.ITextFont_Reset, controls._win32_ITextFont_Reset, tom/ITextFont::Reset, tomApplyLater, tomApplyNow, tomApplyTmp, tomCacheParms, tomDefault, tomDisableSmartFont, tomEnableSmartFont, tomTrackParms, tomUndefined, tomUsePoints, tomUseTwips
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
 - ITextFont::Reset
 - tom/ITextFont::Reset
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
 - ITextFont.Reset
---

# ITextFont::Reset


## -description

Resets the character formatting to the specified values.

## -parameters

### -param Value [in]

Type: <b>long</b>

The kind of reset.  This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomDefault"></a><a id="tomdefault"></a><a id="TOMDEFAULT"></a><dl>
<dt><b>tomDefault</b></dt>
</dl>
</td>
<td width="60%">
Set to the document default character format if this font object is attached to a range; otherwise, set the defaults to the basic TOM engine defaults.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUndefined"></a><a id="tomundefined"></a><a id="TOMUNDEFINED"></a><dl>
<dt><b>tomUndefined</b></dt>
</dl>
</td>
<td width="60%">
Sets all properties to undefined values. This value is valid only for a duplicate (clone) font object.

</td>
</tr>
<tr>
<td width="40%"><a id="tomApplyLater"></a><a id="tomapplylater"></a><a id="TOMAPPLYLATER"></a><dl>
<dt><b>tomApplyLater</b></dt>
</dl>
</td>
<td width="60%">
Allow property values to be set, but don’t apply them to the attached range yet.

</td>
</tr>
<tr>
<td width="40%"><a id="tomApplyNow"></a><a id="tomapplynow"></a><a id="TOMAPPLYNOW"></a><dl>
<dt><b>tomApplyNow</b></dt>
</dl>
</td>
<td width="60%">
Apply the current properties to attached range.

</td>
</tr>
<tr>
<td width="40%"><a id="tomCacheParms"></a><a id="tomcacheparms"></a><a id="TOMCACHEPARMS"></a><dl>
<dt><b>tomCacheParms</b></dt>
</dl>
</td>
<td width="60%">
Do not update the current font with the attached range properties.

</td>
</tr>
<tr>
<td width="40%"><a id="tomTrackParms"></a><a id="tomtrackparms"></a><a id="TOMTRACKPARMS"></a><dl>
<dt><b>tomTrackParms</b></dt>
</dl>
</td>
<td width="60%">
Update the  current font with the attached range properties.

</td>
</tr>
<tr>
<td width="40%"><a id="tomApplyTmp"></a><a id="tomapplytmp"></a><a id="TOMAPPLYTMP"></a><dl>
<dt><b>tomApplyTmp</b></dt>
</dl>
</td>
<td width="60%">
Apply temporary formatting.

</td>
</tr>
<tr>
<td width="40%"><a id="tomDisableSmartFont"></a><a id="tomdisablesmartfont"></a><a id="TOMDISABLESMARTFONT"></a><dl>
<dt><b>tomDisableSmartFont</b></dt>
</dl>
</td>
<td width="60%">
Do not apply smart fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="tomEnableSmartFont"></a><a id="tomenablesmartfont"></a><a id="TOMENABLESMARTFONT"></a><dl>
<dt><b>tomEnableSmartFont</b></dt>
</dl>
</td>
<td width="60%">
Do apply smart fonts.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUsePoints"></a><a id="tomusepoints"></a><a id="TOMUSEPOINTS"></a><dl>
<dt><b>tomUsePoints</b></dt>
</dl>
</td>
<td width="60%">
Use points for floating-point measurements.

</td>
</tr>
<tr>
<td width="40%"><a id="tomUseTwips"></a><a id="tomusetwips"></a><a id="TOMUSETWIPS"></a><dl>
<dt><b>tomUseTwips</b></dt>
</dl>
</td>
<td width="60%">
Use twips for floating-point measurements.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Protected from change.

</td>
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

Calling 
				<b>ITextFont::Reset</b> with <b>tomUndefined</b> sets all properties to undefined values. Thus, applying the font object to a range changes nothing. This applies to a font object that is obtained by the 
				<a href="/windows/desktop/api/tom/nf-tom-itextfont-getduplicate">ITextFont::GetDuplicate</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-getduplicate">GetDuplicate</a>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>