---
UID: NF:peninputpanel.ITextInputPanelEventSink.CorrectionModeChanged
title: ITextInputPanelEventSink::CorrectionModeChanged
author: windows-sdk-content
description: Occurs when the correction comb on the Tablet PC Input Panel has changed modes.
old-location: tablet\itextinputpaneleventsink_correctionmodechanged.htm
old-project: tablet
ms.assetid: 70c4dca4-274f-40ae-b71a-f86a2e8fbd3d
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: 70c4dca4-274f-40ae-b71a-f86a2e8fbd3d, CorrectionModeChanged, CorrectionModeChanged method [Tablet PC], CorrectionModeChanged method [Tablet PC],ITextInputPanelEventSink interface, ITextInputPanelEventSink interface [Tablet PC],CorrectionModeChanged method, ITextInputPanelEventSink.CorrectionModeChanged, ITextInputPanelEventSink::CorrectionModeChanged, peninputpanel/ITextInputPanelEventSink::CorrectionModeChanged, tablet.itextinputpaneleventsink_correctionmodechanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: EventMask
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.CorrectionModeChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: ADAM
---

# ITextInputPanelEventSink::CorrectionModeChanged


## -description



Occurs when the correction comb on the Tablet PC Input Panel has changed modes.




## -parameters




### -param oldCorrectionMode [in]

The previous correction mode, as defined by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.


### -param newCorrectionMode [in]

The current correction mode, as defined by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.


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



<div class="alert"><b>Note</b>  
		In Windows 7, this event is no longer raised.
		</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/e3ef6d65-ca6b-4587-bb21-3d3803a3432a">ITextInputPanelEventSink</a>



<a href="https://msdn.microsoft.com/f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8">ITextInputPanelEventSink::CorrectionModeChanging Method</a>
 

 

