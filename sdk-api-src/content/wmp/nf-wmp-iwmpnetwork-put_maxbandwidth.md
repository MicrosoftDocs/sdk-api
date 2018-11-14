---
UID: NF:wmp.IWMPNetwork.put_maxBandwidth
title: IWMPNetwork::put_maxBandwidth
author: windows-sdk-content
description: The put_maxBandwidth method specifies the maximum allowed bandwidth.
old-location: wmp\iwmpnetwork_put_maxbandwidth.htm
tech.root: WMP
ms.assetid: 7259a5e2-dbc6-4ac0-946e-e79d542edb06
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],put_maxBandwidth method, IWMPNetwork.put_maxBandwidth, IWMPNetwork::put_maxBandwidth, IWMPNetworkput_maxBandwidth, put_maxBandwidth, put_maxBandwidth method [Windows Media Player], put_maxBandwidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_put_maxbandwidth, wmp/IWMPNetwork::put_maxBandwidth
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
 - IWMPNetwork.put_maxBandwidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPNetwork.put_maxBandwidth
: 
---

# IWMPNetwork::put_maxBandwidth


## -description



The <b>put_maxBandwidth</b> method specifies the maximum allowed bandwidth.




## -parameters




### -param lMaxBandwidth [in]

<b>long</b> containing the max bandwidth.


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



This method does not have a default value. The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling <b>IWMPCore::close</b>. Windows Media Player attempts to achieve the highest bandwidth possible. Only in the case of this value being set will any intentional reduction of bandwidth occur.

This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream. An MBR stream contains multiple streams with different bit rates. In some cases, it may be desirable to use a stream with a lower bit rate than the client requires. In this case, specifying a lower bit rate with the <b>IWMPNetwork::put_maxBandwidth</b> method will select a lower bit-rate stream. For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps. Using <b>IWMPNetwork::put_maxBandwidth</b> to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.




## -see-also




<a href="https://msdn.microsoft.com/e6e21995-5dbd-4893-a9f2-6ce918d3fbc4">IWMPCore::close</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/b3b1b845-7aa5-49d7-a9da-52dea06e51c4">IWMPNetwork::get_maxBandwidth</a>
 

 

