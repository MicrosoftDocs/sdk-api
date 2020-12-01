---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceStateChanged
title: ITextInputPanelEventSink::InPlaceStateChanged (peninputpanel.h)
description: Occurs when the In-Place state has changed.
helpviewer_keywords: ["ITextInputPanelEventSink interface [Tablet PC]","InPlaceStateChanged method","ITextInputPanelEventSink.InPlaceStateChanged","ITextInputPanelEventSink::InPlaceStateChanged","InPlaceStateChanged","InPlaceStateChanged method [Tablet PC]","InPlaceStateChanged method [Tablet PC]","ITextInputPanelEventSink interface","bc01ecda-bb9f-40c6-8ac7-ffc4cc89b6a2","peninputpanel/ITextInputPanelEventSink::InPlaceStateChanged","tablet.itextinputpaneleventsink_inplacestatechanged"]
old-location: tablet\itextinputpaneleventsink_inplacestatechanged.htm
tech.root: tablet
ms.assetid: bc01ecda-bb9f-40c6-8ac7-ffc4cc89b6a2
ms.date: 12/05/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InPlaceStateChanged method, ITextInputPanelEventSink.InPlaceStateChanged, ITextInputPanelEventSink::InPlaceStateChanged, InPlaceStateChanged, InPlaceStateChanged method [Tablet PC], InPlaceStateChanged method [Tablet PC],ITextInputPanelEventSink interface, bc01ecda-bb9f-40c6-8ac7-ffc4cc89b6a2, peninputpanel/ITextInputPanelEventSink::InPlaceStateChanged, tablet.itextinputpaneleventsink_inplacestatechanged
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
 - ITextInputPanelEventSink::InPlaceStateChanged
 - peninputpanel/ITextInputPanelEventSink::InPlaceStateChanged
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
 - ITextInputPanelEventSink.InPlaceStateChanged
---

# ITextInputPanelEventSink::InPlaceStateChanged


## -description

Occurs when the In-Place state has changed.

## -parameters

### -param oldInPlaceState [in]

The current state, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

### -param newInPlaceState [in]

The new state that the Input Panel has changed to, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-inplacestate">InPlaceState Enumeration</a>.

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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanging">ITextInputPanelEventSink::InPlaceStateChanging Method</a>