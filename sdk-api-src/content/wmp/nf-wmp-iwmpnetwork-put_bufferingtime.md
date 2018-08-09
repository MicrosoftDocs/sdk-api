---
UID: NF:wmp.IWMPNetwork.put_bufferingTime
title: IWMPNetwork::put_bufferingTime
author: windows-sdk-content
description: The put_bufferingTime method specifies the amount of time in milliseconds allocated for buffering incoming data before playing begins.
old-location: wmp\iwmpnetwork_put_bufferingtime.htm
old-project: WMP
ms.assetid: 9f25992f-e3a0-477b-b445-1f3fb7d9eae1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],put_bufferingTime method, IWMPNetwork.put_bufferingTime, IWMPNetwork::put_bufferingTime, IWMPNetworkput_bufferingTime, put_bufferingTime, put_bufferingTime method [Windows Media Player], put_bufferingTime method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_put_bufferingtime, wmp/IWMPNetwork::put_bufferingTime
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPNetwork.put_bufferingTime
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::put_bufferingTime


## -description



The <b>put_bufferingTime</b> method specifies the amount of time in milliseconds allocated for buffering incoming data before playing begins.




## -parameters




### -param lBufferingTime [in]

<b>long</b> containing the buffering time, which ranges from zero to 60,000 with a default value of 5,000.


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



<a href="https://msdn.microsoft.com/a42a7187-9bf2-4db5-8176-6912e18c4d50">IWMPNetwork::get_bufferingTime</a>
 

 

