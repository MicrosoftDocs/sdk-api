---
UID: NF:peninputpanel.ITextInputPanelEventSink.InputAreaChanging
title: ITextInputPanelEventSink::InputAreaChanging (peninputpanel.h)
description: Occurs when the input area is about to change on the Tablet PC Input Panel.
helpviewer_keywords: ["ITextInputPanelEventSink interface [Tablet PC]","InputAreaChanging method","ITextInputPanelEventSink.InputAreaChanging","ITextInputPanelEventSink::InputAreaChanging","InputAreaChanging","InputAreaChanging method [Tablet PC]","InputAreaChanging method [Tablet PC]","ITextInputPanelEventSink interface","e5f96798-2428-4acd-9d9a-addfdf14bb84","peninputpanel/ITextInputPanelEventSink::InputAreaChanging","tablet.itextinputpaneleventsink_inputareachanging"]
old-location: tablet\itextinputpaneleventsink_inputareachanging.htm
tech.root: tablet
ms.assetid: e5f96798-2428-4acd-9d9a-addfdf14bb84
ms.date: 12/05/2018
ms.keywords: ITextInputPanelEventSink interface [Tablet PC],InputAreaChanging method, ITextInputPanelEventSink.InputAreaChanging, ITextInputPanelEventSink::InputAreaChanging, InputAreaChanging, InputAreaChanging method [Tablet PC], InputAreaChanging method [Tablet PC],ITextInputPanelEventSink interface, e5f96798-2428-4acd-9d9a-addfdf14bb84, peninputpanel/ITextInputPanelEventSink::InputAreaChanging, tablet.itextinputpaneleventsink_inputareachanging
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
 - ITextInputPanelEventSink::InputAreaChanging
 - peninputpanel/ITextInputPanelEventSink::InputAreaChanging
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
 - ITextInputPanelEventSink.InputAreaChanging
---

# ITextInputPanelEventSink::InputAreaChanging


## -description

Occurs when the input area is about to change on the Tablet PC Input Panel.

## -parameters

### -param oldInputArea [in]

The current input area as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

### -param newInputArea [in]

The input area the Input Panel is changing to as defined by the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-panelinputarea">PanelInputArea Enumeration</a>.

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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inputareachanged">ITextInputPanelEventSink::InputAreaChanged Method</a>