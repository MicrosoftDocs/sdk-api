---
UID: NF:peninputpanel.ITextInputPanelEventSink.InputAreaChanged
title: ITextInputPanelEventSink::InputAreaChanged (peninputpanel.h)
description: Occurs when the input area has changed on the Tablet PC Input Panel.
helpviewer_keywords: ["ITextInputPanelEventSink interface [Tablet PC]","InputAreaChanged method","ITextInputPanelEventSink.InputAreaChanged","ITextInputPanelEventSink::InputAreaChanged","InputAreaChanged","InputAreaChanged method [Tablet PC]","InputAreaChanged method [Tablet PC]","ITextInputPanelEventSink interface","b30eaa39-a1f7-4c50-992f-11030bb175f9","peninputpanel/ITextInputPanelEventSink::InputAreaChanged","tablet.itextinputpaneleventsink_inputareachanged"]
old-location: tablet\itextinputpaneleventsink_inputareachanged.htm
tech.root: tablet
ms.assetid: b30eaa39-a1f7-4c50-992f-11030bb175f9
ms.date: 12/05/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InputAreaChanged method, ITextInputPanelEventSink.InputAreaChanged, ITextInputPanelEventSink::InputAreaChanged, InputAreaChanged, InputAreaChanged method [Tablet PC], InputAreaChanged method [Tablet PC],ITextInputPanelEventSink interface, b30eaa39-a1f7-4c50-992f-11030bb175f9, peninputpanel/ITextInputPanelEventSink::InputAreaChanged, tablet.itextinputpaneleventsink_inputareachanged
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
 - ITextInputPanelEventSink::InputAreaChanged
 - peninputpanel/ITextInputPanelEventSink::InputAreaChanged
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
 - ITextInputPanelEventSink.InputAreaChanged
---

# ITextInputPanelEventSink::InputAreaChanged


## -description

Occurs when the input area has changed on the Tablet PC Input Panel.

## -parameters

### -param oldInputArea [in]

The previous input area as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

### -param newInputArea [in]

The current input area as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanging">ITextInputPanelEventSink::InputAreaChanging Method</a>