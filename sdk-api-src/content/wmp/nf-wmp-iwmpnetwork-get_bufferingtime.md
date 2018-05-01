---
UID: NF:wmp.IWMPNetwork.get_bufferingTime
title: IWMPNetwork::get_bufferingTime method
author: windows-driver-content
description: The get_bufferingTime method retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.
old-location: wmp\iwmpnetwork_get_bufferingtime.htm
old-project: WMP
ms.assetid: a42a7187-9bf2-4db5-8176-6912e18c4d50
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWMPNetwork, IWMPNetwork interface [Windows Media Player], get_bufferingTime method, IWMPNetwork::get_bufferingTime, IWMPNetworkget_bufferingTime, get_bufferingTime method [Windows Media Player], get_bufferingTime method [Windows Media Player], IWMPNetwork interface, get_bufferingTime,IWMPNetwork.get_bufferingTime, wmp.iwmpnetwork_get_bufferingtime, wmp/IWMPNetwork::get_bufferingTime
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
-	IWMPNetwork.get_bufferingTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_bufferingTime method


## -description



The <b>get_bufferingTime</b> method retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.




## -parameters




### -param plBufferingTime [out]

Pointer to a <b>long</b> containing the buffering time, which ranges from zero to 60,000 with a default value of 5,000.


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
 




## -see-also




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/9f25992f-e3a0-477b-b445-1f3fb7d9eae1">IWMPNetwork::put_bufferingTime</a>
 

 

