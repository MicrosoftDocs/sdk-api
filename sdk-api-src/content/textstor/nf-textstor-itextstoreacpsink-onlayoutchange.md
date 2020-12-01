---
UID: NF:textstor.ITextStoreACPSink.OnLayoutChange
title: ITextStoreACPSink::OnLayoutChange (textstor.h)
description: ITextStoreACPSink::OnLayoutChange method
helpviewer_keywords: ["ITextStoreACPSink interface [Text Services Framework]","OnLayoutChange method","ITextStoreACPSink.OnLayoutChange","ITextStoreACPSink::OnLayoutChange","OnLayoutChange","OnLayoutChange method [Text Services Framework]","OnLayoutChange method [Text Services Framework]","ITextStoreACPSink interface","_tsf_itextstoreacpsink_onlayoutchange_ref","textstor/ITextStoreACPSink::OnLayoutChange","tsf.itextstoreacpsink_onlayoutchange"]
old-location: tsf\itextstoreacpsink_onlayoutchange.htm
tech.root: TSF
ms.assetid: 2018d3ef-892f-46c0-8dd0-3e27a9f2272c
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnLayoutChange method, ITextStoreACPSink.OnLayoutChange, ITextStoreACPSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onlayoutchange_ref, textstor/ITextStoreACPSink::OnLayoutChange, tsf.itextstoreacpsink_onlayoutchange
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
 - ITextStoreACPSink::OnLayoutChange
 - textstor/ITextStoreACPSink::OnLayoutChange
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
 - ITextStoreACPSink.OnLayoutChange
---

# ITextStoreACPSink::OnLayoutChange


## -description

Called when the layout (on-screen representation) of the document changes.

## -parameters

### -param lcode [in]

Contains a <a href="/windows/win32/api/textstor/ne-textstor-tslayoutcode">TsLayoutCode</a> value that defines the type of change.

### -param vcView [in]

Contains an application-defined cookie that identifies the document. For more information, see <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getactiveview">ITextStoreACP::GetActiveView</a>.

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

If a call to <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITextStoreACP::GetTextExt</a> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITextStoreACP::GetACPFromPoint</a> returns TS_E_NOLAYOUT because the application has not calculated the layout, the application must call <b>ITextStoreACPSink::OnLayoutChange</b> when the layout is available.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITextStoreACP::GetACPFromPoint
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getactiveview">ITextStoreACP::GetActiveView
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITextStoreACP::GetTextExt
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="/windows/win32/api/textstor/ne-textstor-tslayoutcode">TsLayoutCode
      </a>