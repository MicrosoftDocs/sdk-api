---
UID: NF:msctf.ITfContextOwnerServices.OnLayoutChange
title: ITfContextOwnerServices::OnLayoutChange (msctf.h)
description: The ITfContextOwnerServices::OnLayoutChange method is called by the context owner when the on-screen representation of the text stream is updated during a composition.
helpviewer_keywords: ["ITfContextOwnerServices interface [Text Services Framework]","OnLayoutChange method","ITfContextOwnerServices.OnLayoutChange","ITfContextOwnerServices::OnLayoutChange","OnLayoutChange","OnLayoutChange method [Text Services Framework]","OnLayoutChange method [Text Services Framework]","ITfContextOwnerServices interface","_tsf_itfcontextownerservices_onlayoutchange_ref","msctf/ITfContextOwnerServices::OnLayoutChange","tsf.itfcontextownerservices_onlayoutchange"]
old-location: tsf\itfcontextownerservices_onlayoutchange.htm
tech.root: TSF
ms.assetid: a9e17687-6be6-4d2d-ba3a-6c128e71de26
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],OnLayoutChange method, ITfContextOwnerServices.OnLayoutChange, ITfContextOwnerServices::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_onlayoutchange_ref, msctf/ITfContextOwnerServices::OnLayoutChange, tsf.itfcontextownerservices_onlayoutchange
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
 - ITfContextOwnerServices::OnLayoutChange
 - msctf/ITfContextOwnerServices::OnLayoutChange
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
 - ITfContextOwnerServices.OnLayoutChange
---

# ITfContextOwnerServices::OnLayoutChange


## -description

The <b>ITfContextOwnerServices::OnLayoutChange</b> method is called by the context owner when the on-screen representation of the text stream is updated during a composition. Text stream updates include when the position of the window that contains the text is changed or if the screen coordinates of the text change.



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

A call to <b>ITfContextOwnerServices::OnLayoutChange</b> could be in response to a text edit, font size change, window movement/resizing, and so on.

If a call to <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITfContextView::GetTextExt</a> or <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITfContextOwner::GetACPFromPoint</a> fails because the application did not calculate the screen layout (Return Value: TS_E_NOLAYOUT), the application must then call <b>ITfContextOwnerServices::OnLayoutChange</b> when the information is ready.

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getacpfrompoint">ITfContextOwner::GetACPFromPoint
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownerservices">ITfContextOwnerServices</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettextext">ITfContextView::GetTextExt
      </a>
