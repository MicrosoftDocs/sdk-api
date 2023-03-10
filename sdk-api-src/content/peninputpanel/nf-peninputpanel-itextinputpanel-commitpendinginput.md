---
UID: NF:peninputpanel.ITextInputPanel.CommitPendingInput
title: ITextInputPanel::CommitPendingInput (peninputpanel.h)
description: Sends collected ink to the recognizer and posts the recognition result.
helpviewer_keywords: ["652df9e7-5bac-4dc7-bd1a-3934a2bdeb94","CommitPendingInput","CommitPendingInput method [Tablet PC]","CommitPendingInput method [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","CommitPendingInput method","ITextInputPanel.CommitPendingInput","ITextInputPanel::CommitPendingInput","peninputpanel/ITextInputPanel::CommitPendingInput","tablet.itextinputpanel_commitpendinginput"]
old-location: tablet\itextinputpanel_commitpendinginput.htm
tech.root: tablet
ms.assetid: 652df9e7-5bac-4dc7-bd1a-3934a2bdeb94
ms.date: 12/05/2018
ms.keywords: 652df9e7-5bac-4dc7-bd1a-3934a2bdeb94, CommitPendingInput, CommitPendingInput method [Tablet PC], CommitPendingInput method [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],CommitPendingInput method, ITextInputPanel.CommitPendingInput, ITextInputPanel::CommitPendingInput, peninputpanel/ITextInputPanel::CommitPendingInput, tablet.itextinputpanel_commitpendinginput
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
 - ITextInputPanel::CommitPendingInput
 - peninputpanel/ITextInputPanel::CommitPendingInput
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
 - ITextInputPanel.CommitPendingInput
---

# ITextInputPanel::CommitPendingInput


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Sends collected ink to the recognizer and posts the recognition result.



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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

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

The recognition result is sent to the control to which the <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> object is attached.

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpaneleventsink-inplacevisibilitychanged">ITextInputPanelEventSink::InPlaceVisibilityChanged Method</a>
