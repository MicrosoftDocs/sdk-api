---
UID: NF:peninputpanel.ITextInputPanelEventSink.TextInserted
title: ITextInputPanelEventSink::TextInserted (peninputpanel.h)
description: Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel.
helpviewer_keywords: ["61f3c21f-8658-421b-8494-d39a2faacc66","ITextInputPanelEventSink interface [Tablet PC]","TextInserted method","ITextInputPanelEventSink.TextInserted","ITextInputPanelEventSink::TextInserted","TextInserted","TextInserted method [Tablet PC]","TextInserted method [Tablet PC]","ITextInputPanelEventSink interface","peninputpanel/ITextInputPanelEventSink::TextInserted","tablet.itextinputpaneleventsink_textinserted"]
old-location: tablet\itextinputpaneleventsink_textinserted.htm
tech.root: tablet
ms.assetid: 61f3c21f-8658-421b-8494-d39a2faacc66
ms.date: 12/05/2018
ms.keywords: 61f3c21f-8658-421b-8494-d39a2faacc66, ITextInputPanelEventSink interface [Tablet PC],TextInserted method, ITextInputPanelEventSink.TextInserted, ITextInputPanelEventSink::TextInserted, TextInserted, TextInserted method [Tablet PC], TextInserted method [Tablet PC],ITextInputPanelEventSink interface, peninputpanel/ITextInputPanelEventSink::TextInserted, tablet.itextinputpaneleventsink_textinserted
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
 - ITextInputPanelEventSink::TextInserted
 - peninputpanel/ITextInputPanelEventSink::TextInserted
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
 - ITextInputPanelEventSink.TextInserted
---

# ITextInputPanelEventSink::TextInserted


## -description

Occurs when the Tablet PC Input Panel has inserted text into the control with input focus. Provides access to the ink the user entered in the Input Panel.

## -parameters

### -param Ink [in]

Array of <a href="/windows/desktop/tablet/inkdisp-class">Ink</a> objects in the Input Panel.


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

There is a minimum of one <a href="/windows/desktop/tablet/inkdisp-class">Ink</a> object for each line of the Input Panel containing text at the time of insertion.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink">ITextInputPanelEventSink</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-textinserting">ITextInputPanelEventSink::TextInserting Method</a>