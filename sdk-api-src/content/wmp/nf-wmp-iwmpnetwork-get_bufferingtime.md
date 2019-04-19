---
UID: NF:wmp.IWMPNetwork.get_bufferingTime
title: IWMPNetwork::get_bufferingTime (wmp.h)
author: windows-sdk-content
description: The get_bufferingTime method retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.
old-location: wmp\iwmpnetwork_get_bufferingtime.htm
tech.root: WMP
ms.assetid: a42a7187-9bf2-4db5-8176-6912e18c4d50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bufferingTime method, IWMPNetwork.get_bufferingTime, IWMPNetwork::get_bufferingTime, IWMPNetworkget_bufferingTime, get_bufferingTime, get_bufferingTime method [Windows Media Player], get_bufferingTime method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bufferingtime, wmp/IWMPNetwork::get_bufferingTime
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
 - IWMPNetwork.get_bufferingTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPNetwork::get_bufferingTime


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




<a href="https://msdn.microsoft.com/en-us/library/Dd563461(v=VS.85).aspx">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563484(v=VS.85).aspx">IWMPNetwork::put_bufferingTime</a>
 

 

