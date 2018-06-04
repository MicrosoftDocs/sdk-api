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

# IWRdsGraphicsChannel::Open


## -description



    Called to open a channel. When the channel is completely open and ready for use, you must call the <a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -parameters




### -param pChannelEvents [in]

Type: <b><a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/59802a2d-bdb0-4792-b667-5095d4a02b06">IWRdsGraphicsChannelEvents</a> interface that will receive notifications relating to the channel created.


### -param pOpenContext [in]

Type: <b>IUnknown*</b>

A user-defined interface pointer that is passed as the <i>pOpenContext</i> parameter in the <a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d1e88b4-3dff-4f88-a6de-abc02da57ece">IWRdsGraphicsChannel</a>



<a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">IWRdsGraphicsChannelEvents::OnChannelOpened</a>
 

 

