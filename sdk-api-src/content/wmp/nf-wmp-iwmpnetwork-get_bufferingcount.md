---
UID: NF:wmp.IWMPNetwork.get_bufferingCount
title: IWMPNetwork::get_bufferingCount
author: windows-sdk-content
description: The get_bufferingCount method retrieves the number of times buffering occurred during playback.
old-location: wmp\iwmpnetwork_get_bufferingcount.htm
old-project: WMP
ms.assetid: 9ba9be8d-9b2b-4620-8572-317555d51bdf
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_bufferingCount method, IWMPNetwork.get_bufferingCount, IWMPNetwork::get_bufferingCount, IWMPNetworkget_bufferingCount, get_bufferingCount, get_bufferingCount method [Windows Media Player], get_bufferingCount method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_bufferingcount, wmp/IWMPNetwork::get_bufferingCount
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
-	IWMPNetwork.get_bufferingCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPNetwork::get_bufferingCount


## -description



The <b>get_bufferingCount</b> method retrieves the number of times buffering occurred during playback.




## -parameters




### -param plBufferingCount [out]

Pointer to a <b>long</b> containing the buffering count.


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

Buffering only applies to streaming content. This method retrieves valid information only during run time when the URL for playback is set by using the <b>IWMPCore::put_URL</b> method.




## -see-also




<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">IWMPCore::put_URL</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

