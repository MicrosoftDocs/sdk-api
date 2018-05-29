---
UID: NF:wmp.IWMPNetwork.get_bandWidth
title: IWMPNetwork::get_bandWidth
author: windows-sdk-content
description: The get_bandWidth method retrieves the current bandwidth of the media item.
old-location: wmp\iwmpnetwork_get_bandwidth.htm
old-project: WMP
ms.assetid: 910356d8-3d43-4516-ad30-b0ed288e5098
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bandWidth method, IWMPNetwork.get_bandWidth, IWMPNetwork::get_bandWidth, IWMPNetworkget_bandWidth, get_bandWidth, get_bandWidth method [Windows Media Player], get_bandWidth method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bandwidth, wmp/IWMPNetwork::get_bandWidth
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPNetwork.get_bandWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_bandWidth


## -description



The <b>get_bandWidth</b> method retrieves the current bandwidth of the media item.




## -parameters




### -param plBandwidth [out]

Pointer to a <b>long</b> containing the bandwidth.


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



The value retrieved through <b>IWMPCore::put_URL</b> will be zero if the URL is not set. This method is only valid for streaming media.




## -see-also




<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

