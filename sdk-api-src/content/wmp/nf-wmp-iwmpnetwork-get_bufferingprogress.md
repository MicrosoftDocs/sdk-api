---
UID: NF:wmp.IWMPNetwork.get_bufferingProgress
title: IWMPNetwork::get_bufferingProgress
author: windows-sdk-content
description: The get_bufferingProgress method retrieves the percentage of buffering completed.
old-location: wmp\iwmpnetwork_get_bufferingprogress.htm
tech.root: WMP
ms.assetid: 5c8cc541-3fc2-49b8-8a1a-f4959989aafe
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bufferingProgress method, IWMPNetwork.get_bufferingProgress, IWMPNetwork::get_bufferingProgress, IWMPNetworkget_bufferingProgress, get_bufferingProgress, get_bufferingProgress method [Windows Media Player], get_bufferingProgress method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bufferingprogress, wmp/IWMPNetwork::get_bufferingProgress
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
 - IWMPNetwork.get_bufferingProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPNetwork::get_bufferingProgress


## -description



The <b>get_bufferingProgress</b> method retrieves the percentage of buffering completed.




## -parameters




### -param plBufferingProgress [out]

Pointer to a <b>long</b> containing the buffering progress.


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



Each time playback is stopped and restarted, the value retrieved from this method is zero. It is not reset if playback is paused.

Buffering only applies to streaming content. This method retrieves valid information only during run time when the URL for playback is set using the <b>IWMPCore::put_URL</b> method.

Use the <b>IWMPEvents::Buffering</b> event to determine when buffering starts or stops.




## -see-also




<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/3e379c92-b400-48ad-a3d3-82ed3cd3f396">IWMPEvents::Buffering</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

