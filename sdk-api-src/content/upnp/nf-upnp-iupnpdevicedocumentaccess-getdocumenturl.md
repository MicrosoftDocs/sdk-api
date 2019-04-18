---
UID: NF:upnp.IUPnPDeviceDocumentAccess.GetDocumentURL
title: IUPnPDeviceDocumentAccess::GetDocumentURL (upnp.h)
author: windows-sdk-content
description: The GetDocumentURL method returns the URL from which the device description document can be loaded.
old-location: upnp\iupnpdevicedocumentaccess_getdocumenturl.htm
tech.root: upnp
ms.assetid: 7845e543-47c6-4751-8e29-2508b2adb090
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDocumentURL, GetDocumentURL method [UPnP APIs], GetDocumentURL method [UPnP APIs],IUPnPDeviceDocumentAccess interface, IUPnPDeviceDocumentAccess interface [UPnP APIs],GetDocumentURL method, IUPnPDeviceDocumentAccess.GetDocumentURL, IUPnPDeviceDocumentAccess::GetDocumentURL, _upnp_iupnpdevicedocumentaccess_getdocumenturl, upnp.iupnpdevicedocumentaccess_getdocumenturl, upnp/IUPnPDeviceDocumentAccess::GetDocumentURL
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
 - IUPnPDeviceDocumentAccess.GetDocumentURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceDocumentAccess::GetDocumentURL


## -description


The 
<b>GetDocumentURL</b> method returns the URL from which the device description document can be loaded.


## -parameters




### -param pbstrDocument [out]

Receives the URL from which the device description document can be downloaded.


## -returns



If the method succeeds, the return value is as specified above. Otherwise, the method returns one of the COM error codes specified in winerror.h.




## -remarks



This method does not support scripting.




## -see-also




<a href="https://msdn.microsoft.com/25bd3abd-b270-4609-93bb-a786ccaa95dd">IUPnPDescriptionDocument</a>



<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/6d71425e-3e33-44e0-845a-4bcd05939d24">IUPnPDeviceDocumentAccess</a>
 

 

