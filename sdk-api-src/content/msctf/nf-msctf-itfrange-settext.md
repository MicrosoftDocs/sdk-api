---
UID: NF:msctf.ITfRange.SetText
title: ITfRange::SetText (msctf.h)
description: The ITfRange::SetText method replaces the content covered by the range of text.
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","SetText method","ITfRange.SetText","ITfRange::SetText","SetText","SetText method [Text Services Framework]","SetText method [Text Services Framework]","ITfRange interface","_tsf_itfrange_settext_ref","msctf/ITfRange::SetText","tsf.itfrange_settext"]
old-location: tsf\itfrange_settext.htm
tech.root: TSF
ms.assetid: 797d96a1-0250-4e8d-a4bd-31152fd6eca7
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],SetText method, ITfRange.SetText, ITfRange::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITfRange interface, _tsf_itfrange_settext_ref, msctf/ITfRange::SetText, tsf.itfrange_settext
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfRange::SetText
 - msctf/ITfRange::SetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.SetText
---

# ITfRange::SetText


## -description

The <b>ITfRange::SetText</b> method replaces the content covered by the range of text. For an empty range object, the method results in an insertion at the location of the range. If the new content is an empty string (<i>cch</i> = 0), the method deletes the existing content within the range.

## -parameters

### -param ec [in]

Identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param dwFlags [in]

Specifies optional behavior for correction of content. If set to the value of <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_ST_CORRECTION</a>, then the operation is a correction of the existing content, not a creation of new content, and original text properties are preserved.

### -param pchText [in]

Pointer to a buffer that contains the text to replace the range contents.

### -param cch [in]

Contains the number of characters in <i>pchText</i>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_COMPOSITION_REJECTED</b></dt>
</dl>
</td>
<td width="60%">
The context owner rejected a default composition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read/write lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_RANGE_NOT_COVERED</b></dt>
</dl>
</td>
<td width="60%">
The range is not within the active composition of the caller.

</td>
</tr>
</table>

## -remarks

When a range covers multiple regions, call <b>ITfRange::SetText</b> on each region separately. Otherwise, the method can fail.

By default, text services start and end a temporary composition that covers the range, to ensure that context owners consistently recognize compositions over edited text. If the composition owner rejects a default composition, then the method returns TF_E_COMPOSITION_REJECTED. Default compositions are only created if the caller has not already started one. If the caller has an active composition, the call fails.

The <a href="/windows/desktop/TSF/miscellaneous-framework-constants">TF_CHAR_EMBEDDED</a> object placeholder character might not be passed into this method. <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded">ITfRange::InsertEmbedded</a> should be used instead.

For inserting text, the <a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-inserttextatselection">ITFInsertAtSelection:InsertTextAtSelection</a> method does not require a selection range to be allocated, and avoids the requirement that the range match the selection.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-inserttextatselection">ITFInsertAtSelection:InsertTextAtSelection
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-gettext">ITfRange::GetText
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded">ITfRange::InsertEmbedded
      </a>



<a href="/windows/desktop/TSF/miscellaneous-framework-constants">Miscellaneous Framework Constants</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>