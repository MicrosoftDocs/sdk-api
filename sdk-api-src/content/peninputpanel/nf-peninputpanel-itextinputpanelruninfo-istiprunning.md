---
UID: NF:peninputpanel.ITextInputPanelRunInfo.IsTipRunning
title: ITextInputPanelRunInfo::IsTipRunning (peninputpanel.h)
description: Indicates if the Tablet PC Input Panel is running at the time the method is called.
helpviewer_keywords: ["3d82dd05-c03c-4c97-8d41-84a74e3c3a8a","ITextInputPanelRunInfo interface [Tablet PC]","IsTipRunning method","ITextInputPanelRunInfo.IsTipRunning","ITextInputPanelRunInfo::IsTipRunning","IsTipRunning","IsTipRunning method [Tablet PC]","IsTipRunning method [Tablet PC]","ITextInputPanelRunInfo interface","peninputpanel/ITextInputPanelRunInfo::IsTipRunning","tablet.itextinputpanelruninfo_istiprunning"]
old-location: tablet\itextinputpanelruninfo_istiprunning.htm
tech.root: tablet
ms.assetid: 3d82dd05-c03c-4c97-8d41-84a74e3c3a8a
ms.date: 12/05/2018
ms.keywords: 3d82dd05-c03c-4c97-8d41-84a74e3c3a8a, ITextInputPanelRunInfo interface [Tablet PC],IsTipRunning method, ITextInputPanelRunInfo.IsTipRunning, ITextInputPanelRunInfo::IsTipRunning, IsTipRunning, IsTipRunning method [Tablet PC], IsTipRunning method [Tablet PC],ITextInputPanelRunInfo interface, peninputpanel/ITextInputPanelRunInfo::IsTipRunning, tablet.itextinputpanelruninfo_istiprunning
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
 - ITextInputPanelRunInfo::IsTipRunning
 - peninputpanel/ITextInputPanelRunInfo::IsTipRunning
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
 - ITextInputPanelRunInfo.IsTipRunning
---

# ITextInputPanelRunInfo::IsTipRunning


## -description

Indicates if the Tablet PC Input Panel is running at the time the method is called.

## -parameters

### -param pfRunning [out]

<b>TRUE</b> if the Input Panel was running, otherwise <b>FALSE</b>.

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
The <i>pfRunning</i> parameter has been set appropriately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfRunning</i> parameter was <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo">ITextInputPanelRunInfo Interface</a>