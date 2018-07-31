---
UID: NN:upnp.IUPnPDeviceDocumentAccess
title: IUPnPDeviceDocumentAccess
author: windows-sdk-content
description: The IUPnPDeviceDocumentAccess interface enables an application to obtain the URL of the device description document.
old-location: upnp\iupnpdevicedocumentaccess.htm
old-project: UPnP
ms.assetid: 6d71425e-3e33-44e0-845a-4bcd05939d24
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUPnPDeviceDocumentAccess, IUPnPDeviceDocumentAccess interface [UPnP APIs], IUPnPDeviceDocumentAccess interface [UPnP APIs],described, _upnp_iupnpdevicedocumentaccess, upnp.iupnpdevicedocumentaccess, upnp/IUPnPDeviceDocumentAccess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IUPnPDeviceDocumentAccess
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceDocumentAccess interface


## -description


The 
<b>IUPnPDeviceDocumentAccess</b> interface enables an application to obtain the URL of the device description document.
<div class="alert"><b>Note</b>  This interface does not support scripting.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceDocumentAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPDeviceDocumentAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceDocumentAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7845e543-47c6-4751-8e29-2508b2adb090">GetDocumentURL</a>
</td>
<td align="left" width="63%">
Returns the URL from which the device description document can be loaded.

</td>
</tr>
</table> 

