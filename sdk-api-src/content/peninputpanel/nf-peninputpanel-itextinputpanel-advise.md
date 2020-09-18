---
UID: NF:peninputpanel.ITextInputPanel.Advise
title: ITextInputPanel::Advise (peninputpanel.h)
description: Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.
helpviewer_keywords: ["4ea32572-84e6-4230-a634-fc83cb86601f","Advise","Advise method [Tablet PC]","Advise method [Tablet PC]","ITextInputPanel interface","ITextInputPanel interface [Tablet PC]","Advise method","ITextInputPanel.Advise","ITextInputPanel::Advise","peninputpanel/ITextInputPanel::Advise","tablet.itextinputpanel_advise"]
old-location: tablet\itextinputpanel_advise.htm
tech.root: tablet
ms.assetid: 4ea32572-84e6-4230-a634-fc83cb86601f
ms.date: 12/05/2018
ms.keywords: 4ea32572-84e6-4230-a634-fc83cb86601f, Advise, Advise method [Tablet PC], Advise method [Tablet PC],ITextInputPanel interface, ITextInputPanel interface [Tablet PC],Advise method, ITextInputPanel.Advise, ITextInputPanel::Advise, peninputpanel/ITextInputPanel::Advise, tablet.itextinputpanel_advise
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
 - ITextInputPanel::Advise
 - peninputpanel/ITextInputPanel::Advise
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
 - ITextInputPanel.Advise
---

# ITextInputPanel::Advise


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel</a> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration">IInputPanelConfiguration</a>.

]


Establishes an advisory connection between the Tablet PC Input Panel and the specified sink object.

## -parameters

### -param EventSink [in]

Reference to the sink object to receive event notifications from the Input Panel.

### -param EventMask

A bitwise value of the <a href="/windows/win32/api/peninputpanel/ne-peninputpanel-eventmask">EventMask Enumeration</a>, indicating the events of interest.

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

<a href="/windows/win32/api/peninputpanel/ne-peninputpanel-eventmask">EventMask Enumeration</a>



<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a>



<a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-unadvise">ITextInputPanel::Unadvise Method</a>