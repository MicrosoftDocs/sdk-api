---
UID: NF:peninputpanel.ITextInputPanelEventSink.CorrectionModeChanging
title: ITextInputPanelEventSink::CorrectionModeChanging (peninputpanel.h)
description: Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.
helpviewer_keywords: ["CorrectionModeChanging","CorrectionModeChanging method [Tablet PC]","CorrectionModeChanging method [Tablet PC]","ITextInputPanelEventSink interface","ITextInputPanelEventSink interface [Tablet PC]","CorrectionModeChanging method","ITextInputPanelEventSink.CorrectionModeChanging","ITextInputPanelEventSink::CorrectionModeChanging","f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8","peninputpanel/ITextInputPanelEventSink::CorrectionModeChanging","tablet.itextinputpaneleventsink_correctionmodechanging"]
old-location: tablet\itextinputpaneleventsink_correctionmodechanging.htm
tech.root: tablet
ms.assetid: f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8
ms.date: 12/05/2018
ms.keywords: CorrectionModeChanging, CorrectionModeChanging method [Tablet PC], CorrectionModeChanging method [Tablet PC],ITextInputPanelEventSink interface, ITextInputPanelEventSink interface [Tablet PC],CorrectionModeChanging method, ITextInputPanelEventSink.CorrectionModeChanging, ITextInputPanelEventSink::CorrectionModeChanging, f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8, peninputpanel/ITextInputPanelEventSink::CorrectionModeChanging, tablet.itextinputpaneleventsink_correctionmodechanging
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
 - ITextInputPanelEventSink::CorrectionModeChanging
 - peninputpanel/ITextInputPanelEventSink::CorrectionModeChanging
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
 - ITextInputPanelEventSink.CorrectionModeChanging
---

# ITextInputPanelEventSink::CorrectionModeChanging


## -description

Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.

## -parameters

### -param oldCorrectionMode [in]

The current correction mode, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.

### -param newCorrectionMode [in]

The correction mode the Input Panel is changing to, as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-correctionmode">CorrectionMode Enumeration</a>.

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

<div class="alert"><b>Note</b>  In Windows 7, this event no longer is raised.		
		</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink">ITextInputPanelEventSink</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-correctionmodechanged">ITextInputPanelEventSink::CorrectionModeChanged Method</a>