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

# IWRdsGraphicsChannelEvents::OnChannelOpened


## -description


Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened. The RemoteFX graphics services calls the <a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a> method to open a channel. You must call the <b>OnChannelOpened</b> method to notify the RemoteFX graphics services that the channel is open and ready for use, or if an error occurs.


## -parameters




### -param OpenResult [in]

An <b>HRESULT</b> value that specifies the result of the open operation. If this parameter contains <b>S_OK</b>, <i>pOpenContext</i> is valid.


### -param pOpenContext [in]

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a>



<a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>
 

 

