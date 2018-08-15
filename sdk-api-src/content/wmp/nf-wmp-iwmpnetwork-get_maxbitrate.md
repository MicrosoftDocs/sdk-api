---
UID: NF:wmp.IWMPNetwork.get_maxBitRate
title: IWMPNetwork::get_maxBitRate
author: windows-sdk-content
description: The get_maxBitRate method retrieves the maximum possible video bit rate.
old-location: wmp\iwmpnetwork_get_maxbitrate.htm
old-project: WMP
ms.assetid: 42917ca3-07d3-4d32-a2f3-5f0ef9d387d7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_maxBitRate method, IWMPNetwork.get_maxBitRate, IWMPNetwork::get_maxBitRate, IWMPNetworkget_maxBitRate, get_maxBitRate, get_maxBitRate method [Windows Media Player], get_maxBitRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_maxbitrate, wmp/IWMPNetwork::get_maxBitRate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
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
 - IWMPNetwork.get_maxBitRate
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_maxBitRate


## -description



The <b>get_maxBitRate</b> method retrieves the maximum possible video bit rate.




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
 




## -see-also




<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

