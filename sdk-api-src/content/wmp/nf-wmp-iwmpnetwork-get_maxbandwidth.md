---
UID: NF:wmp.IWMPNetwork.get_maxBandwidth
title: IWMPNetwork::get_maxBandwidth
author: windows-sdk-content
description: The get_maxBandwidth method retrieves the maximum allowed bandwidth.
old-location: wmp\iwmpnetwork_get_maxbandwidth.htm
tech.root: WMP
ms.assetid: b3b1b845-7aa5-49d7-a9da-52dea06e51c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_maxBandwidth method, IWMPNetwork.get_maxBandwidth, IWMPNetwork::get_maxBandwidth, IWMPNetworkget_maxBandwidth, get_maxBandwidth, get_maxBandwidth method [Windows Media Player], get_maxBandwidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_maxbandwidth, wmp/IWMPNetwork::get_maxBandwidth
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
 - IWMPNetwork.get_maxBandwidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPNetwork::get_maxBandwidth


## -description



The <b>get_maxBandwidth</b> method retrieves the maximum allowed bandwidth.




## -parameters




### -param lMaxBandwidth [out]

Pointer to a <b>long</b> containing the maximum bandwidth.


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




<a href="https://msdn.microsoft.com/e6e21995-5dbd-4893-a9f2-6ce918d3fbc4">IWMPCore::close</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/7259a5e2-dbc6-4ac0-946e-e79d542edb06">IWMPNetwork::put_maxBandwidth</a>
 

 

