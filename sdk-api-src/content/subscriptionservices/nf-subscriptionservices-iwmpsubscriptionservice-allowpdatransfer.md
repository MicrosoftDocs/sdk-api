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

# IWMPSubscriptionService::allowPDATransfer


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>allowPDATransfer</b> method is implemented by the online store's plug-in to manage permission for Windows Media Player to synchronize content with a device.




## -parameters




### -param hwnd [in]

A handle to a window in which the plug-in can display a user interface.


### -param pPlaylist [in, out]

Pointer to a playlist object.


### -param pfAllowTransfer [out]

Pointer to a <b>BOOL</b>. If true, copying to a device is allowed.


## -returns



The method returns an <b>HRESULT</b>.




## -remarks



Your code should not perform lengthy operations synchronously when Windows Media Player calls this method.

When Windows Media Player calls your plug-in's <b>allowPDATransfer</b> method, it passes a pointer to a playlist, which contains items from your online store. Your <b>allowPDATransfer</b> method must remove any items from the playlist that should not be synchronized with a device.

The situations in which Windows Media Player calls <b>allowPDATranfer</b> differ between versions of Windows Media Player.

Windows Media Player 9 Series and Windows Media Player 10 call <b>allowPDATransfer</b> automatically in certain situations. For example, if the user attempts to synchronize a list of tracks with a device, and some of those tracks do not have permission to be synchronized, Windows Media Player calls <b>allowPDATransfer</b>.

Windows Media Player 11 never calls <b>allowPDATransfer</b> automatically. That is, Windows Media Player 11 calls <b>allowPDATransfer</b> only when the user explicitly requests synchronization rights. For example, the user might request a synchronization rights by choosing a command from the context menu of an information icon.

Do not rely on <b>allowPDATransfer</b> being called each time a track is synchronized with a device. Instead, implement <a href="https://msdn.microsoft.com/64ab5548-b562-44e4-9798-8f14d3ed653b">IWMPSubscriptionService2::prepareForSync</a>.




## -see-also




<a href="https://msdn.microsoft.com/cb9d0f20-d5ca-4db9-adcc-0a803f97f196">IWMPSubscriptionService Interface</a>
 

 

