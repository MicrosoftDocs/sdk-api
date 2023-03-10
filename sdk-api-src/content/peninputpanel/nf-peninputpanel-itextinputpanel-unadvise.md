---
UID: NF:peninputpanel.ITextInputPanel.Unadvise
title: ITextInputPanel::Unadvise (peninputpanel.h)
description: Terminates an advisory connection previously established through ITextInputPanel::Advise Method.
helpviewer_keywords: ["8ea2c112-0d57-4da6-89da-5afe57ff2346","ITextInputPanel interface [Tablet PC]","Unadvise method","ITextInputPanel.Unadvise","ITextInputPanel::Unadvise","Unadvise","Unadvise method [Tablet PC]","Unadvise method [Tablet PC]","ITextInputPanel interface","peninputpanel/ITextInputPanel::Unadvise","tablet.itextinputpanel_unadvise"]
old-location: tablet\itextinputpanel_unadvise.htm
tech.root: tablet
ms.assetid: 8ea2c112-0d57-4da6-89da-5afe57ff2346
ms.date: 12/05/2018
ms.keywords: 8ea2c112-0d57-4da6-89da-5afe57ff2346, ITextInputPanel interface [Tablet PC],Unadvise method, ITextInputPanel.Unadvise, ITextInputPanel::Unadvise, Unadvise, Unadvise method [Tablet PC], Unadvise method [Tablet PC],ITextInputPanel interface, peninputpanel/ITextInputPanel::Unadvise, tablet.itextinputpanel_unadvise
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
 - ITextInputPanel::Unadvise
 - peninputpanel/ITextInputPanel::Unadvise
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
 - ITextInputPanel.Unadvise
---

# ITextInputPanel::Unadvise


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Terminates an advisory connection previously established through <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-advise">ITextInputPanel::Advise Method</a>.

## -parameters

### -param EventSink [in]

Reference to the sink object currently receiving event notifications from the Input Panel.

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



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-advise">ITextInputPanel::Advise Method</a>