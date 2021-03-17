---
UID: NF:textstor.ITextStoreAnchorSink.OnLayoutChange
title: ITextStoreAnchorSink::OnLayoutChange (textstor.h)
description: The ITextStoreAnchorSink::OnLayoutChange method is called when the layout (on-screen representation) of the document changes.
helpviewer_keywords: ["ITextStoreAnchorSink interface [Text Services Framework]","OnLayoutChange method","ITextStoreAnchorSink.OnLayoutChange","ITextStoreAnchorSink::OnLayoutChange","OnLayoutChange","OnLayoutChange method [Text Services Framework]","OnLayoutChange method [Text Services Framework]","ITextStoreAnchorSink interface","_tsf_itextstoreanchorsink_onlayoutchange_ref","textstor/ITextStoreAnchorSink::OnLayoutChange","tsf.itextstoreanchorsink_onlayoutchange"]
old-location: tsf\itextstoreanchorsink_onlayoutchange.htm
tech.root: TSF
ms.assetid: 22629ca6-5701-4f6f-b797-bb71c8d31da6
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnLayoutChange method, ITextStoreAnchorSink.OnLayoutChange, ITextStoreAnchorSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onlayoutchange_ref, textstor/ITextStoreAnchorSink::OnLayoutChange, tsf.itextstoreanchorsink_onlayoutchange
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
 - ITextStoreAnchorSink::OnLayoutChange
 - textstor/ITextStoreAnchorSink::OnLayoutChange
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
 - ITextStoreAnchorSink.OnLayoutChange
---

# ITextStoreAnchorSink::OnLayoutChange


## -description

The <b>ITextStoreAnchorSink::OnLayoutChange</b> method is called when the layout (on-screen representation) of the document changes.

## -parameters

### -param lcode [in]

Contains a <a href="/windows/win32/api/textstor/ne-textstor-tslayoutcode">TsLayoutCode</a> value that defines the type of change.

### -param vcView [in]

Contains an application-defined cookie that identifies the document. For more information, see <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getactiveview">ITextStoreAnchor::GetActiveView</a>.

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
</table>

## -remarks

A layout change can be in response to a change to the text, font size, window movement, window resizing, or other change that affects the displayed text.

If a call to <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-gettextext">ITextStoreAnchor::GetTextExt</a> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getanchorfrompoint">ITextStoreAnchor::GetAnchorFromPoint</a> returns TS_E_NOLAYOUT because the application has not calculated the layout, the application must call <b>ITextStoreAnchorSink::OnLayoutChange</b> when the layout is available.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getactiveview">ITextStoreAnchor::GetActiveView
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getanchorfrompoint">ITextStoreAnchor::GetAnchorFromPoint
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-gettextext">ITextStoreAnchor::GetTextExt
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a>



<a href="/windows/win32/api/textstor/ne-textstor-tslayoutcode">TsLayoutCode
      </a>