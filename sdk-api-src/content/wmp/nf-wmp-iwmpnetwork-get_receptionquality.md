---
UID: NF:wmp.IWMPNetwork.get_receptionQuality
title: IWMPNetwork::get_receptionQuality method
author: windows-driver-content
description: The get_receptionQuality method retrieves the percentage of packets received in the last 30 seconds.
old-location: wmp\iwmpnetwork_get_receptionquality.htm
old-project: WMP
ms.assetid: 835f56a4-26d3-480c-bf3e-49c269e9cc5a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], get_receptionQuality method, IWMPNetwork::get_receptionQuality, IWMPNetworkget_receptionQuality, get_receptionQuality method [Windows Media Player], get_receptionQuality method [Windows Media Player], IWMPNetwork interface, get_receptionQuality,IWMPNetwork.get_receptionQuality, wmp.iwmpnetwork_get_receptionquality, wmp/IWMPNetwork::get_receptionQuality
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPNetwork.get_receptionQuality
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_receptionQuality method


## -description



The <b>get_receptionQuality</b> method retrieves the percentage of packets received in the last 30 seconds.




## -parameters




### -param plReceptionQuality [out]

Pointer to a <b>long</b> containing the reception quality.


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



The number of packets received, lost, and recovered during streaming is monitored once every second. The <b>get_receptionQuality</b> method retrieves the percentage of packets not lost during the last 30 seconds.

Each time playback is stopped and restarted, the value retrieved from this method is reset to zero. The value is not reset if playback is paused.

This method retrieves valid information only during run time when the URL for playback is set by using the <b>IWMPCore::put_URL</b> method.




## -see-also




<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

