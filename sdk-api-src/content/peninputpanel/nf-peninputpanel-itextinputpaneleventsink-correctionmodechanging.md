---
UID: NF:peninputpanel.ITextInputPanelEventSink.CorrectionModeChanging
title: ITextInputPanelEventSink::CorrectionModeChanging
author: windows-sdk-content
description: Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.
old-location: tablet\itextinputpaneleventsink_correctionmodechanging.htm
tech.root: tablet
ms.assetid: f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CorrectionModeChanging, CorrectionModeChanging method [Tablet PC], CorrectionModeChanging method [Tablet PC],ITextInputPanelEventSink interface, ITextInputPanelEventSink interface [Tablet PC],CorrectionModeChanging method, ITextInputPanelEventSink.CorrectionModeChanging, ITextInputPanelEventSink::CorrectionModeChanging, f20b77dc-a04f-4bd3-9aa0-3a0c3d98e4a8, peninputpanel/ITextInputPanelEventSink::CorrectionModeChanging, tablet.itextinputpaneleventsink_correctionmodechanging
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
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITextInputPanelEventSink.CorrectionModeChanging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextInputPanelEventSink::CorrectionModeChanging


## -description



Occurs when the correction comb on the Tablet PC Input Panel is about to change modes.




## -parameters




### -param oldCorrectionMode [in]

The current correction mode, as defined by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.


### -param newCorrectionMode [in]

The correction mode the Input Panel is changing to, as defined by the <a href="https://msdn.microsoft.com/133d2012-e43c-490a-b126-b7670ea7acf8">CorrectionMode Enumeration</a>.


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




<a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a>



<a href="https://msdn.microsoft.com/e3ef6d65-ca6b-4587-bb21-3d3803a3432a">ITextInputPanelEventSink</a>



<a href="https://msdn.microsoft.com/70c4dca4-274f-40ae-b71a-f86a2e8fbd3d">ITextInputPanelEventSink::CorrectionModeChanged Method</a>
 

 

