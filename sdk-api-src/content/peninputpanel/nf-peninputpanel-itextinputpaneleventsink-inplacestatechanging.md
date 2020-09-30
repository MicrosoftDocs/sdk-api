---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceStateChanging
title: ITextInputPanelEventSink::InPlaceStateChanging (peninputpanel.h)
description: Occurs when the In-Place state is about to change.
helpviewer_keywords: ["866fcd8d-775c-4dc0-824f-6817767247d9","ITextInputPanelEventSink interface [Tablet PC]","InPlaceStateChanging method","ITextInputPanelEventSink.InPlaceStateChanging","ITextInputPanelEventSink::InPlaceStateChanging","InPlaceStateChanging","InPlaceStateChanging method [Tablet PC]","InPlaceStateChanging method [Tablet PC]","ITextInputPanelEventSink interface","peninputpanel/ITextInputPanelEventSink::InPlaceStateChanging","tablet.itextinputpaneleventsink_inplacestatechanging"]
old-location: tablet\itextinputpaneleventsink_inplacestatechanging.htm
tech.root: tablet
ms.assetid: 866fcd8d-775c-4dc0-824f-6817767247d9
ms.date: 12/05/2018
ms.keywords: 866fcd8d-775c-4dc0-824f-6817767247d9, ITextInputPanelEventSink interface [Tablet PC],InPlaceStateChanging method, ITextInputPanelEventSink.InPlaceStateChanging, ITextInputPanelEventSink::InPlaceStateChanging, InPlaceStateChanging, InPlaceStateChanging method [Tablet PC], InPlaceStateChanging method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::InPlaceStateChanging, tablet.itextinputpaneleventsink_inplacestatechanging
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextInputPanelEventSink::InPlaceStateChanging
 - peninputpanel/ITextInputPanelEventSink::InPlaceStateChanging
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.InPlaceStateChanging
---

# ITextInputPanelEventSink::InPlaceStateChanging


## -description

Occurs when the In-Place state is about to change.

## -parameters

### -param oldInPlaceState [in]

The current state, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

### -param newInPlaceState [in]

The new state that the Input Panel is changing to, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

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
</table>

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink">ITextInputPanelEventSink</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanged">ITextInputPanelEventSink::InPlaceStateChanged Method</a>