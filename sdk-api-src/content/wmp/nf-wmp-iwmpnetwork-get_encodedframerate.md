---
UID: NF:wmp.IWMPNetwork.get_encodedFrameRate
title: IWMPNetwork::get_encodedFrameRate
author: windows-sdk-content
description: The get_encodedFrameRate method retrieves the video frame rate specified by the content author.
old-location: wmp\iwmpnetwork_get_encodedframerate.htm
tech.root: WMP
ms.assetid: d42133cf-3b81-4d22-b83d-d8a5756d9d9c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMPNetwork interface [Windows Media Player],get_encodedFrameRate method, IWMPNetwork.get_encodedFrameRate, IWMPNetwork::get_encodedFrameRate, IWMPNetworkget_encodedFrameRate, get_encodedFrameRate, get_encodedFrameRate method [Windows Media Player], get_encodedFrameRate method [Windows Media Player],IWMPNetwork interface, wmp.iwmpnetwork_get_encodedframerate, wmp/IWMPNetwork::get_encodedFrameRate
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
 - IWMPNetwork.get_encodedFrameRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPNetwork::get_encodedFrameRate


## -description



The <b>get_encodedFrameRate</b> method retrieves the video frame rate specified by the content author.




## -parameters




### -param plFrameRate [out]

Pointer to a <b>long</b> containing the frame rate in frames per second (fps).


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



<a href="https://msdn.microsoft.com/1521c462-b054-46d6-8646-4d20a836eadc">IWMPNetwork::get_frameRate</a>
 

 

