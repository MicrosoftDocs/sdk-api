---
UID: NF:upnp.IUPnPHttpHeaderControl.AddRequestHeaders
title: IUPnPHttpHeaderControl::AddRequestHeaders (upnp.h)
author: windows-sdk-content
description: Adds the supplied HTTP header to an HTTP request.
old-location: upnp\iupnphttpheadercontrol_addrequestheaders.htm
tech.root: upnp
ms.assetid: e44f83de-eaf6-4b16-a70e-64f4daffc6b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddRequestHeaders, AddRequestHeaders method [UPnP APIs], AddRequestHeaders method [UPnP APIs],IUPnPHttpHeaderControl interface, IUPnPHttpHeaderControl interface [UPnP APIs],AddRequestHeaders method, IUPnPHttpHeaderControl.AddRequestHeaders, IUPnPHttpHeaderControl::AddRequestHeaders, upnp.iupnphttpheadercontrol_addrequestheaders, upnp/IUPnPHttpHeaderControl::AddRequestHeaders
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IUPnPHttpHeaderControl.AddRequestHeaders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPHttpHeaderControl::AddRequestHeaders


## -description


The <a href="https://msdn.microsoft.com/aed33117-9bfd-4a23-998f-4b8d040d6e3b">IUPnPHttpHeaderControl</a>::<b>AddRequestHeaders</b> method adds the supplied HTTP header to an HTTP request.


## -parameters




### -param bstrHttpHeaders [in]

String value that contains the HTTP header to attach to the request. For example, "User-Agent: DLNADOC/1.50\r\n".


<div class="alert"><b>Note</b>  For Windows 7 and Windows Server 2008 R2, only the User Agent HTTP header is supported.</div>
<div> </div>



## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/aed33117-9bfd-4a23-998f-4b8d040d6e3b">IUPnPHttpHeaderControl</a>
 

 

