---
UID: NF:upnp.IUPnPService.get_Id
title: IUPnPService::get_Id (upnp.h)
author: windows-sdk-content
description: The Id property specifies the service ID for the service.
old-location: upnp\iupnpservice_id.htm
tech.root: upnp
ms.assetid: daa2ed07-8ee5-4e1f-84f4-77f58d4958e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPService interface [UPnP APIs],get_Id method, IUPnPService.get_Id, IUPnPService::get_Id, _upnp_iupnpservice_id, get_Id, get_Id method [UPnP APIs], get_Id method [UPnP APIs],IUPnPService interface, upnp.iupnpservice_id, upnp/IUPnPService::get_Id
ms.topic: method
f1_keywords: 
 - "upnp/IUPnPService.get_Id"
dev_langs:
 - c++
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
 - IUPnPService.get_Id
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPService::get_Id


## -description


The 
<b>Id</b> property specifies the service ID for the service.


## -parameters




### -param pbstrId [out]

Receives a reference to the service ID. Release this string with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required..


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>
 

 

