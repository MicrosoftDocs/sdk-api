---
UID: NN:peninputpanel.ITextInputPanelEventSink
title: ITextInputPanelEventSink (peninputpanel.h)

description: Defines methods that handle the ITextInputPanel Interface events.
old-location: tablet\itextinputpaneleventsink.htm
tech.root: tablet
ms.assetid: e3ef6d65-ca6b-4587-bb21-3d3803a3432a

ms.date: 12/05/2018
ms.keywords: ITextInputPanelEventSink, ITextInputPanelEventSink interface [Tablet PC], ITextInputPanelEventSink interface [Tablet PC],described, e3ef6d65-ca6b-4587-bb21-3d3803a3432a, peninputpanel/ITextInputPanelEventSink, tablet.itextinputpaneleventsink
ms.topic: interface
f1_keywords: 
 - "peninputpanel/ITextInputPanelEventSink"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextInputPanelEventSink interface


## -description



Defines methods that handle the <a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a> events.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextInputPanelEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextInputPanelEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextInputPanelEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanged">CorrectionModeChanged</a>
</td>
<td align="left" width="63%">
Occurs when the correction comb on the Tablet PC Input Panel has changed modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanging">CorrectionModeChanging</a>
</td>
<td align="left" width="63%">
Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanged">InPlaceSizeChanged</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place Input Panel size has changed due to a user resize, auto growth, or an input area change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacesizechanging">InPlaceSizeChanging</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place Input Panel size is about to change due to a user resize, auto growth, or an input area change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanged">InPlaceStateChanged</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place state has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacestatechanging">InPlaceStateChanging</a>
</td>
<td align="left" width="63%">
Occurs when the In-Place state is about to change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged">InPlaceVisibilityChanged</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel has switched between visible and invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanging">InPlaceVisibilityChanging</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel is about to switch between visible and invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanged">InputAreaChanged</a>
</td>
<td align="left" width="63%">
Occurs when the input area has changed on the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanging">InputAreaChanging</a>
</td>
<td align="left" width="63%">
Occurs when the input area is about to change on the Tablet PC Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserted">TextInserted</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserting">TextInserting</a>
</td>
<td align="left" width="63%">
Occurs when the Tablet PC Input Panel is about to insert text into the control with input focus. Provides access to the ink the user entered in the Input Panel.

</td>
</tr>
</table> 


## -remarks



This element is declared in Peninputpanel.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>
 

 

