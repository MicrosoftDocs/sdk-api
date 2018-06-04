---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IWMReaderNetworkConfig2::SetAutoReconnectLimit


## -description



The <b>SetAutoReconnectLimit</b> method sets the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection. This feature, called Fast Reconnect, applies only to content being streamed from a server running Windows Media Services.




## -parameters




### -param dwAutoReconnectLimit [in]

Specifies the maximum number of times the reader object will attempt to reconnect. To disable automatic reconnection, set this value to zero.


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



The method configures the Fast Reconnect feature, which enables the reader object to reconnect to the server automatically if it loses the connection. When possible, playback resumes at the same point in the stream. The accuracy may depend on whether the source file is indexed. For live content, there may be a gap in the stream.

The reader only tries to reconnect if the interruption is unexpected. For example, it does not try to reconnect if the server denies access because of an authentication failure, if the server terminates the connection because of client inactivity, if the server administrator terminates the connection, and so forth.

This method is equivalent to setting the WMReconnect modifier in the URL. For example:

mms://MyServer/MyVideo.wmv?WMReconnect=5




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/8d0b794c-b3bf-4ec5-ac68-9666e73f7a6e">IWMReaderNetworkConfig2::GetAutoReconnectLimit</a>
 

 

