---
UID: NF:wmp.IWMPSyncDevice3.cancelEstimation
title: IWMPSyncDevice3::cancelEstimation
author: windows-sdk-content
description: The cancelEstimation method cancels an estimation that was previously initiated by estimateSyncSize.
old-location: wmp\iwmpsyncdevice3_cancelestimation.htm
tech.root: WMP
ms.assetid: 82e87e44-0a38-43c0-bbed-011581ae8a85
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPSyncDevice3 interface [Windows Media Player],cancelEstimation method, IWMPSyncDevice3.cancelEstimation, IWMPSyncDevice3::cancelEstimation, cancelEstimation, cancelEstimation method [Windows Media Player], cancelEstimation method [Windows Media Player],IWMPSyncDevice3 interface, wmp.iwmpsyncdevice3_cancelestimation, wmp/IWMPSyncDevice3::cancelEstimation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 12
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSyncDevice3.cancelEstimation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPSyncDevice3::cancelEstimation


## -description



The <b>cancelEstimation</b> method cancels an estimation that was previously initiated by <a href="https://msdn.microsoft.com/en-us/library/Dd563715(v=VS.85).aspx">estimateSyncSize</a>.




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




<a href="https://msdn.microsoft.com/en-us/library/Dd563713(v=VS.85).aspx">IWMPSyncDevice3 Interface</a>
 

 

