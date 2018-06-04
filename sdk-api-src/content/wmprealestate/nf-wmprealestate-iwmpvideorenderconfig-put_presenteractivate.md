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

# IWMPVideoRenderConfig::put_presenterActivate


## -description



The <b>put_presenterActivate</b> method provides Windows Media Player with an activation object for a custom video presenter.




## -parameters




### -param pActivate [in]

A pointer to an <b>IMFActivate</b> interface that Windows Media Player or another Windows component will use to activate the custom video presenter.


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



In certain situations, Windows Media Player uses a video pipeline that includes the enhanced video renderer (EVR). The EVR is a system component that allows other components and applications to provide custom plug-ins that perform tasks like video mixing and video presenting.

An application that embeds Windows Media Player can provide a custom video presenter for the EVR by calling <b>put_presenterActivate</b>. The application must create its own activation object that implements the <b>IMFActivate</b> interface. The application provides Windows Media Player with that interface in the <i>pActivate</i> parameter. When Windows Media Player or another system component needs to create an instance of the custom presenter, it calls the <b>ActivateObject</b> method of the <b>IMFActivate</b> interface provided by the application.

The activation object is responsible for initializing the custom presenter. The nature of the initialization and the format of any context data required for the initialization are completely under the control of those who develop the custom presenter and the activation object.

The EVR, custom presenters, activation objects, and the <b>IMFActivate</b> interface are documented in the Microsoft Media Foundation SDK, which is part of the Microsoft Windows SDK. You can download the Windows SDK from the <a href="http://go.microsoft.com/fwlink/p/?linkid=884">MSDN Download and Code Center</a>.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/60318e68-89dd-4505-a703-3de4d5442236">IWMPVideoRenderConfig Interface</a>
 

 

