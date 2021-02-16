---
UID: NF:textstor.ITextStoreAnchor.SetText
title: ITextStoreAnchor::SetText (textstor.h)
description: The ITextStoreAnchor::SetText method sets the text selection between two supplied anchor locations.
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","SetText method","ITextStoreAnchor.SetText","ITextStoreAnchor::SetText","SetText","SetText method [Text Services Framework]","SetText method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::SetText","tsf.itextstoreanchor_settext"]
old-location: tsf\itextstoreanchor_settext.htm
tech.root: TSF
ms.assetid: 03beac03-cd09-4e03-b700-d96741e4932b
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],SetText method, ITextStoreAnchor.SetText, ITextStoreAnchor::SetText, SetText, SetText method [Text Services Framework], SetText method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::SetText, tsf.itextstoreanchor_settext
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::SetText
 - textstor/ITextStoreAnchor::SetText
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
 - ITextStoreAnchor.SetText
---

# ITextStoreAnchor::SetText


## -description

The <b>ITextStoreAnchor::SetText</b> method sets the text selection between two supplied anchor locations.

## -parameters

### -param dwFlags [in]

If set to the value of TS_ST_CORRECTION, the text is a transform (correction) of existing content, and any special text markup information (metadata) is retained, such as .wav file data or a language identifier. The client defines the type of markup information to be retained.

### -param paStart [in]

Pointer to the anchor at the start of the range of text to replace.

### -param paEnd [in]

Pointer to the anchor at the end of the range of text to replace. Must always follow or be at the same position as <i>paStart</i>.

### -param pchText [in]

Pointer to the replacement text. The text string does not have to be <b>NULL</b> terminated, because the text character count is specified in the <i>cch</i> parameter.

### -param cch [in]

Specifies the number of characters in the replacement text.

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
The method could not instantiate one of the anchors <i>paStart</i> or <i>paEnd</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The location of <i>paStart</i> or <i>paEnd</i> is outside of the document text.

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

Applications should start a composition by first using <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">ITextStoreAnchor::InsertTextAtSelection</a>. <b>ITextStoreAnchor::SetText</b> should be used only within an existing composition. If there is no active composition at the time <b>SetText</b> is called, the TSF manager creates a composition that lasts just long enough to wrap the call to <b>SetText</b>.

Callers must hold a write lock obtained through <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestlock">ITextStoreAnchor::RequestLock</a>. Otherwise, <b>ITextStoreAnchor::SetText</b> will fail with TS_E_NOLOCK.

If <i>paStart</i> is at the same location as <i>paEnd</i>, then the operation is an insertion, and no existing text will be removed.

TS_CHAR_EMBEDDED cannot be passed into this method. For <a href="/windows/desktop/TSF/embedded-objects">embedded objects</a>, use <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembedded">ITextStoreAnchor::InsertEmbedded</a> instead.

This method will fail if the range of text replaced covers any region boundary. Instead, callers should make multiple calls to the method, one for each region.

## -see-also

<a href="/windows/desktop/TSF/compositions">Compositions</a>



<a href="/windows/desktop/TSF/embedded-objects">Embedded Objects</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembedded">ITextStoreAnchor::InsertEmbedded
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestlock">ITextStoreAnchor::RequestLock
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-ontextchange">ITextStoreAnchorSink::OnTextChange
      </a>



<a href="/windows/desktop/TSF/miscellaneous-text-store-constants">Miscellaneous Text Store Constants
      </a>