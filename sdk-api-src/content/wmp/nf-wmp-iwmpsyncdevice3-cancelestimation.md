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

# IWMPSyncDevice3::cancelEstimation


## -description



The <b>cancelEstimation</b> method cancels an estimation that was previously initiated by <a href="https://msdn.microsoft.com/49b07233-df9d-4fd0-836e-62b992408018">estimateSyncSize</a>.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



When you call this method, Windows Media Player raises the<a href="https://msdn.microsoft.com/2fb45a13-d82b-48b6-b9bb-46409f33a33f"> IWMPEvents4::SyncEstimationComplete</a> event with an <b>HRESULT</b> of E_ABORT.




## -see-also




<a href="https://msdn.microsoft.com/4fc8d307-38d4-4f46-bd8c-b05d60d9d0fa">IWMPSyncDevice3 Interface</a>
 

 

