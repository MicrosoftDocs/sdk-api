---
UID: NF:peninputpanel.ITextInputPanelEventSink.CorrectionModeChanged
title: ITextInputPanelEventSink::CorrectionModeChanged (peninputpanel.h)
description: Occurs when the correction comb on the Tablet PC Input Panel has changed modes.
helpviewer_keywords: ["70c4dca4-274f-40ae-b71a-f86a2e8fbd3d","CorrectionModeChanged","CorrectionModeChanged method [Tablet PC]","CorrectionModeChanged method [Tablet PC]","ITextInputPanelEventSink interface","ITextInputPanelEventSink interface [Tablet PC]","CorrectionModeChanged method","ITextInputPanelEventSink.CorrectionModeChanged","ITextInputPanelEventSink::CorrectionModeChanged","peninputpanel/ITextInputPanelEventSink::CorrectionModeChanged","tablet.itextinputpaneleventsink_correctionmodechanged"]
old-location: tablet\itextinputpaneleventsink_correctionmodechanged.htm
tech.root: tablet
ms.assetid: 70c4dca4-274f-40ae-b71a-f86a2e8fbd3d
ms.date: 12/05/2018
ms.keywords: 70c4dca4-274f-40ae-b71a-f86a2e8fbd3d, CorrectionModeChanged, CorrectionModeChanged method [Tablet PC], CorrectionModeChanged method [Tablet PC],ITextInputPanelEventSink interface, ITextInputPanelEventSink interface [Tablet PC],CorrectionModeChanged method, ITextInputPanelEventSink.CorrectionModeChanged, ITextInputPanelEventSink::CorrectionModeChanged, peninputpanel/ITextInputPanelEventSink::CorrectionModeChanged, tablet.itextinputpaneleventsink_correctionmodechanged
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
 - ITextInputPanelEventSink::CorrectionModeChanged
 - peninputpanel/ITextInputPanelEventSink::CorrectionModeChanged
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
 - ITextInputPanelEventSink.CorrectionModeChanged
---

# ITextInputPanelEventSink::CorrectionModeChanged


## -description

Occurs when the correction comb on the Tablet PC Input Panel has changed modes.

## -parameters

### -param oldCorrectionMode [in]

The previous correction mode, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.

### -param newCorrectionMode [in]

The current correction mode, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.

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

<div class="alert"><b>Note</b>  In Windows 7, this event is no longer raised.
		</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink">ITextInputPanelEventSink</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanging">ITextInputPanelEventSink::CorrectionModeChanging Method</a>