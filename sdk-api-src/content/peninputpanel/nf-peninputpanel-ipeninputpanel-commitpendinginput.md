---
UID: NF:peninputpanel.IPenInputPanel.CommitPendingInput
title: IPenInputPanel::CommitPendingInput (peninputpanel.h)
description: Deprecated. The PenInputPanel has been replaced by the Text Input Panel (TIP).Sends collected ink to the recognizer and posts the recognition result.
helpviewer_keywords: ["4dd0f334-174a-495c-b363-149960ae2253","CommitPendingInput","CommitPendingInput method [Tablet PC]","CommitPendingInput method [Tablet PC]","IPenInputPanel interface","IPenInputPanel interface [Tablet PC]","CommitPendingInput method","IPenInputPanel.CommitPendingInput","IPenInputPanel::CommitPendingInput","peninputpanel/IPenInputPanel::CommitPendingInput","tablet.peninputpanel_commitpendinginput"]
old-location: tablet\peninputpanel_commitpendinginput.htm
tech.root: tablet
ms.assetid: 4dd0f334-174a-495c-b363-149960ae2253
ms.date: 12/05/2018
ms.keywords: 4dd0f334-174a-495c-b363-149960ae2253, CommitPendingInput, CommitPendingInput method [Tablet PC], CommitPendingInput method [Tablet PC],IPenInputPanel interface, IPenInputPanel interface [Tablet PC],CommitPendingInput method, IPenInputPanel.CommitPendingInput, IPenInputPanel::CommitPendingInput, peninputpanel/IPenInputPanel::CommitPendingInput, tablet.peninputpanel_commitpendinginput
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPenInputPanel::CommitPendingInput
 - peninputpanel/IPenInputPanel::CommitPendingInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IPenInputPanel.CommitPendingInput
---

# IPenInputPanel::CommitPendingInput


## -description

Deprecated.  The <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> has been replaced by the <a href="/windows/desktop/tablet/text-input-panel-reference">Text Input Panel (TIP)</a>.

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

The writing pad sends the collected ink to the recognizer and clears the writing pad. The East Asian multibox sends recognized characters and clears multiboxes. The recognition result is sent to the control to which the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is attached.

If there is no pending input or the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel">CurrentPanel</a> property is <a href="/windows/desktop/api/peninputpanel/ne-peninputpanel-paneltype">Keyboard</a>, <b>CommitPendingInput</b> does nothing. If the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is inactive, calling this method generates an error.

Starting with Microsoft Windows XP Tablet PC Edition 2005, ink is recognized as the user is entering. Therefore, the <b>CommitPendingInput</b> function sends the already recognized text to the edit control; it does not force recognition to occur.

Starting with Windows XP Tablet PC Edition 2005, if the <a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a> object is inactive, <b>CommitPendingInput</b> does not generate an error, it simply returns.

## -see-also

<a href="../peninputpanel/nn-peninputpanel-ipeninputpanel.md">IPenInputPanel</a>



<a href="/windows/desktop/tablet/peninputpanel-class">PenInputPanel</a>
