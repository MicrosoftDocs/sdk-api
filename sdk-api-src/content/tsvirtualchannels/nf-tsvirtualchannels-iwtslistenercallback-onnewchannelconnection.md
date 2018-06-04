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

# IWTSListenerCallback::OnNewChannelConnection


## -description


Allows the Remote Desktop Connection (RDC) client plug-in to accept or deny a connection request for an 
    incoming connection.


## -parameters




### -param pChannel [in]

An <a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannel</a> object that 
      represents the incoming connection. This object will only be connected if the connection is accepted by this 
      method.


### -param data




### -param pbAccept [out]

Indicates whether the connection should be accepted. Receives <b>TRUE</b> if the 
      connection should be accepted or <b>FALSE</b> otherwise.


### -param ppCallback [out]

Receives an 
      <a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a> object that 
      receives notifications for the connection. This object is created by the plug-in.


#### - Data [in]

This parameter is not implemented and is reserved for future use.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ecc673ec-1bea-4e7c-b1b5-a2342445f6cf">DVC Client Plug-in Example</a>



<a href="https://msdn.microsoft.com/b5f1d74d-31e6-4447-82ab-6dd3ad9957fd">IWTSListenerCallback</a>



<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannel</a>



<a href="https://msdn.microsoft.com/d90c6f80-ed4c-4b99-af85-d2c5816ade85">IWTSVirtualChannelCallback</a>
 

 

