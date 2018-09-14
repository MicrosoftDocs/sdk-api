---
UID: NF:wmp.IWMPNetwork.get_bitRate
title: IWMPNetwork::get_bitRate
author: windows-sdk-content
description: The get_bitRate method retrieves the current bit rate being received.
old-location: wmp\iwmpnetwork_get_bitrate.htm
tech.root: WMP
ms.assetid: dfac8b29-47d9-4cee-801b-f43fa2bba6ed
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bitRate method, IWMPNetwork.get_bitRate, IWMPNetwork::get_bitRate, IWMPNetworkget_bitRate, get_bitRate, get_bitRate method [Windows Media Player], get_bitRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bitrate, wmp/IWMPNetwork::get_bitRate
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
 - IWMPNetwork.get_bitRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPNetwork::get_bitRate


## -description



The <b>get_bitRate</b> method retrieves the current bit rate being received.




## -parameters




### -param plBitRate [out]

Pointer to a <b>long</b> containing the bit rate.


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



The value retrieved by this method is a combination of the bit rates of both video and audio streams.




## -see-also




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

