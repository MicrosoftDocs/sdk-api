---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceSizeChanged
title: ITextInputPanelEventSink::InPlaceSizeChanged (peninputpanel.h)
description: Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change.
helpviewer_keywords: ["ITextInputPanelEventSink interface [Tablet PC]","InPlaceSizeChanged method","ITextInputPanelEventSink.InPlaceSizeChanged","ITextInputPanelEventSink::InPlaceSizeChanged","InPlaceSizeChanged","InPlaceSizeChanged method [Tablet PC]","InPlaceSizeChanged method [Tablet PC]","ITextInputPanelEventSink interface","dd1f7cba-0a0f-49da-ad67-5c2e01830750","peninputpanel/ITextInputPanelEventSink::InPlaceSizeChanged","tablet.itextinputpaneleventsink_inplacesizechanged"]
old-location: tablet\itextinputpaneleventsink_inplacesizechanged.htm
tech.root: tablet
ms.assetid: dd1f7cba-0a0f-49da-ad67-5c2e01830750
ms.date: 12/05/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InPlaceSizeChanged method, ITextInputPanelEventSink.InPlaceSizeChanged, ITextInputPanelEventSink::InPlaceSizeChanged, InPlaceSizeChanged, InPlaceSizeChanged method [Tablet PC], InPlaceSizeChanged method [Tablet PC],ITextInputPanelEventSink interface, dd1f7cba-0a0f-49da-ad67-5c2e01830750, peninputpanel/ITextInputPanelEventSink::InPlaceSizeChanged, tablet.itextinputpaneleventsink_inplacesizechanged
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
 - ITextInputPanelEventSink::InPlaceSizeChanged
 - peninputpanel/ITextInputPanelEventSink::InPlaceSizeChanged
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
 - ITextInputPanelEventSink.InPlaceSizeChanged
---

# ITextInputPanelEventSink::InPlaceSizeChanged


## -description

Occurs when the in-place Input Panel size has changed due to a user resize, auto growth, or an input area change.

## -parameters

### -param oldBoundingRectangle [in]

The bounding rectangle that represents the previous size of the Input Panel.

### -param newBoundingRectangle [in]

The bounding rectangle that represents the current size of the Input Panel.

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

## -remarks

Actions causing the Input Panel to change size include changing the screen resolution or DPI settings, rotating the tablet screen, changing the input language, the user explicitly resizing the Input Panel, and changing the theme.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink">ITextInputPanelEventSink</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging">ITextInputPanelEventSink::InPlaceSizeChanging Method</a>