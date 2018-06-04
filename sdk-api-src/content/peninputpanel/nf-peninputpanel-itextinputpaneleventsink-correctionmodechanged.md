---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

