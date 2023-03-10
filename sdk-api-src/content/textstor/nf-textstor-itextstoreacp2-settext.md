---
UID: NF:textstor.ITextStoreACP2.SetText
title: ITextStoreACP2::SetText (textstor.h)
description: Sets the text selection to the supplied character positions.
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","SetText method","ITextStoreACP2.SetText","ITextStoreACP2::SetText","SetText","SetText method [Text Services Framework]","SetText method [Text Services Framework]","ITextStoreACP2 interface","acpNewEnd","acpOldEnd","acpStart","textstor/ITextStoreACP2::SetText","tsf.itextstoreacp2_settext"]
old-location: tsf\itextstoreacp2_settext.htm
tech.root: TSF
ms.assetid: a00b8273-1690-4cf5-899f-afcb1092bfe8
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],SetText method, ITextStoreACP2.SetText, ITextStoreACP2::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITextStoreACP2 interface, acpNewEnd, acpOldEnd, acpStart, textstor/ITextStoreACP2::SetText, tsf.itextstoreacp2_settext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::SetText
 - textstor/ITextStoreACP2::SetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.SetText
---

# ITextStoreACP2::SetText


## -description

Sets the text selection to the supplied character positions.

## -parameters

### -param dwFlags [in]

If set to the value of <b>TS_ST_CORRECTION</b>, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. The client defines the type of markup information to be retained.

### -param acpStart [in]

Specifies the starting character position of the text to replace.

### -param acpEnd [in]

Specifies the ending character position of the text to replace. This parameter is ignored if the value is 1.

### -param pchText [in]

Specifies the pointer to the replacement text. The text string does not have to be <b>NULL</b> terminated, because the text character count is specified in the <i>cch</i> parameter.

### -param cch [in]

Specifies the number of characters in the replacement text.

### -param pChange [out]

Pointer to a <a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a> structure with the following data.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="acpStart"></a><a id="acpstart"></a><a id="ACPSTART"></a><dl>
<dt><b>acpStart</b></dt>
</dl>
</td>
<td width="60%">
The starting application character position before the text is inserted into the document.

</td>
</tr>
<tr>
<td width="40%"><a id="acpOldEnd"></a><a id="acpoldend"></a><a id="ACPOLDEND"></a><dl>
<dt><b>acpOldEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending position before the text is inserted into the document. This value is the same as <i>acpStart</i> for an insertion point. If this value is different from <i>acpStart</i>, then text was selected prior to the text insertion.

</td>
</tr>
<tr>
<td width="40%"><a id="acpNewEnd"></a><a id="acpnewend"></a><a id="ACPNEWEND"></a><dl>
<dt><b>acpNewEnd</b></dt>
</dl>
</td>
<td width="60%">
The ending position after the text insertion occurred.

</td>
</tr>
</table>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The <i>acpStart</i> or <i>acpEnd</i> parameter is outside of the document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
The document is read-only. Content cannot be modified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_REGION</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to modify text across a region boundary.

</td>
</tr>
</table>

## -remarks

Applications should start a composition by first using <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-inserttextatselection">InsertTextAtSelection</a>. <b>SetText</b> should be used only within an existing composition. If there is no active composition at the time <b>SetText</b> is called, the TSF manager creates a composition that lasts just long enough to wrap the call to <b>SetText</b>.

The <i>acpStart</i> and <i>acpEnd</i> character positions cannot be outside the document range.

Applications should not call the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a> method in response to this method.

This method should call the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-setselection">SetSelection</a> method to select the text to be changed. After successfully executing the <b>SetSelection</b> method, this method then calls the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-inserttextatselection">InsertTextAtSelection</a> method to perform the actual text change.

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/TSF/miscellaneous-text-store-constants">Miscellaneous Text Store Constants
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacpsink-ontextchange">OnTextChange</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_textchange">TS_TEXTCHANGE</a>