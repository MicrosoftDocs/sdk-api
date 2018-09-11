---
UID: NF:upnp.IUPnPDescriptionDocument.RootDevice
title: IUPnPDescriptionDocument::RootDevice
author: windows-sdk-content
description: The RootDevice method returns the root device of the currently loaded document's device tree.
old-location: upnp\iupnpdescriptiondocument_rootdevice.htm
tech.root: UPnP
ms.assetid: 0caa4f1e-0c74-4654-be26-6178aefa3ee4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],RootDevice method, IUPnPDescriptionDocument.RootDevice, IUPnPDescriptionDocument::RootDevice, RootDevice, RootDevice method [UPnP APIs], RootDevice method [UPnP APIs],IUPnPDescriptionDocument interface, _upnp_iupnpdescriptiondocument_rootdevice, upnp.iupnpdescriptiondocument_rootdevice, upnp/IUPnPDescriptionDocument::RootDevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
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
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.RootDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDescriptionDocument::RootDevice


## -description


The 
<b>RootDevice</b> method returns the root device of the currently loaded document's device tree.


## -parameters




### -param ppudRootDevice [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that describes the device. This reference must be released when it is no longer required.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Do not use 
<b>RootDevice</b> unless a device description is first loaded using either 
<a href="https://msdn.microsoft.com/02ae8af2-44f2-4b7c-a426-f2a26c43da37">IUPnPDescriptionDocument::Load</a> or 
<a href="https://msdn.microsoft.com/bfb1d833-13e8-4ffe-832d-f6640a42055a">IUPnPDescriptionDocument::LoadAsync</a>. The search operation only searches in the currently loaded device description.




## -see-also




<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>
 

 

