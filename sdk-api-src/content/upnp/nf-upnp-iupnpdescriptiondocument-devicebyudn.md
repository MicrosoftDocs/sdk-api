---
UID: NF:upnp.IUPnPDescriptionDocument.DeviceByUDN
title: IUPnPDescriptionDocument::DeviceByUDN
author: windows-sdk-content
description: The DeviceByUDN method returns the device with the specified unique device name (UDN) contained within the loaded description document.
old-location: upnp\iupnpdescriptiondocument_devicebyudn.htm
old-project: upnp
ms.assetid: 0f8ae379-3ec6-4fe2-ae7b-fe3750a5d4c3
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: DeviceByUDN, DeviceByUDN method [UPnP APIs], DeviceByUDN method [UPnP APIs],IUPnPDescriptionDocument interface, IUPnPDescriptionDocument interface [UPnP APIs],DeviceByUDN method, IUPnPDescriptionDocument.DeviceByUDN, IUPnPDescriptionDocument::DeviceByUDN, _upnp_iupnpdescriptiondocument_devicebyudn, upnp.iupnpdescriptiondocument_devicebyudn, upnp/IUPnPDescriptionDocument::DeviceByUDN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.DeviceByUDN
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDescriptionDocument::DeviceByUDN


## -description


The 
<b>DeviceByUDN</b> method returns the device with the specified unique device name (UDN) contained within the loaded description document.


## -parameters




### -param bstrUDN [in]

Specifies the UDN of the device.


### -param ppudDevice [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that describes the device. This reference must be released when it is no longer used.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Use 
<b>DeviceByUDN</b> after loading the device description using 
<a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">IUPnPDescriptionDocument::Load</a> or 
<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a>. The 
<a href="https://msdn.microsoft.com/592939fa-ebce-419f-a813-ecbbe788fd8e">IUPnPDescriptionDocument::ReadyState</a> property returns READYSTATE_COMPLETED.

Do not use 
<b>DeviceByUDN</b> unless a device description is first loaded using either 
<a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">IUPnPDescriptionDocument::Load</a> or 
<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a>. The search operation only searches in the currently loaded device description.




## -see-also




<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>
 

 

