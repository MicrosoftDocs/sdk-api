---
UID: NF:peninputpanel.ITextInputPanelEventSink.InPlaceVisibilityChanging
title: ITextInputPanelEventSink::InPlaceVisibilityChanging (peninputpanel.h)
description: Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.
helpviewer_keywords: ["957e1c24-3eee-4a6f-9157-961e3d6914b7","ITextInputPanelEventSink interface [Tablet PC]","InPlaceVisibilityChanging method","ITextInputPanelEventSink.InPlaceVisibilityChanging","ITextInputPanelEventSink::InPlaceVisibilityChanging","InPlaceVisibilityChanging","InPlaceVisibilityChanging method [Tablet PC]","InPlaceVisibilityChanging method [Tablet PC]","ITextInputPanelEventSink interface","peninputpanel/ITextInputPanelEventSink::InPlaceVisibilityChanging","tablet.itextinputpaneleventsink_inplacevisibilitychanging"]
old-location: tablet\itextinputpaneleventsink_inplacevisibilitychanging.htm
tech.root: tablet
ms.assetid: 957e1c24-3eee-4a6f-9157-961e3d6914b7
ms.date: 12/05/2018
ms.keywords: 957e1c24-3eee-4a6f-9157-961e3d6914b7, ITextInputPanelEventSink interface [Tablet PC],InPlaceVisibilityChanging method, ITextInputPanelEventSink.InPlaceVisibilityChanging, ITextInputPanelEventSink::InPlaceVisibilityChanging, InPlaceVisibilityChanging, InPlaceVisibilityChanging method [Tablet PC], InPlaceVisibilityChanging method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::InPlaceVisibilityChanging, tablet.itextinputpaneleventsink_inplacevisibilitychanging
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
 - ITextInputPanelEventSink::InPlaceVisibilityChanging
 - peninputpanel/ITextInputPanelEventSink::InPlaceVisibilityChanging
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
 - ITextInputPanelEventSink.InPlaceVisibilityChanging
---

# ITextInputPanelEventSink::InPlaceVisibilityChanging


## -description

Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.

## -parameters

### -param oldVisible [in]

<b>TRUE</b> if the Input Panel is changing from visible to invisible, otherwise <b>FALSE</b>.

### -param newVisible [in]

<b>TRUE</b> if the Input Panel is changing from invisible to visible, otherwise <b>FALSE</b>.

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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged">ITextInputPanelEventSink::InPlaceVisibilityChanged Method</a>