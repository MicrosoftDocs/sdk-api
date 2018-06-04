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

# IWTSVirtualChannelManager::CreateListener


## -description


Returns an instance of a listener object that listens on a specific endpoint.


## -parameters




### -param pszChannelName [in]

The endpoint name on which the listener will listen. This is a string value, the length of which is limited to <b>MAX_PATH</b> number of characters.


### -param uFlags




### -param pListenerCallback [in, optional]

Returns a listener callback (<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>)  that will receive notifications for incoming connections.


### -param ppListener [out, optional]

An instance of the <a href="https://msdn.microsoft.com/af0dda9a-0d18-4f44-ac13-0bf2b903d34e">IWTSListener</a> object.


#### - ulFlags [in]

This parameter is reserved and must be set to zero.




## -returns



Returns <b>S_OK</b> on success.




## -see-also




<a href="https://msdn.microsoft.com/af0dda9a-0d18-4f44-ac13-0bf2b903d34e">IWTSListener</a>



<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>



<a href="https://msdn.microsoft.com/289f76b8-dbb5-4f80-98e9-f39f7946494b">IWTSVirtualChannelManager</a>
 

 

