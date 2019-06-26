---
UID: NF:upnp.IUPnPServiceDocumentAccess.GetDocumentURL
title: IUPnPServiceDocumentAccess::GetDocumentURL (upnp.h)
author: windows-sdk-content
description: GetDocumentURL method retrieves the Service Control Protocol Description (SCPD) URL for a service object. Using this URL, the UPnP control point can download the complete SCPD document.
old-location: upnp\iupnpservicedocumentaccess_getdocumenturl.htm
tech.root: upnp
ms.assetid: 57AF4510-89D6-4DD5-B164-1478A5C27E20
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDocumentURL, GetDocumentURL method [UPnP APIs], GetDocumentURL method [UPnP APIs],IUPnPServiceDocumentAccess interface, IUPnPServiceDocumentAccess interface [UPnP APIs],GetDocumentURL method, IUPnPServiceDocumentAccess.GetDocumentURL, IUPnPServiceDocumentAccess::GetDocumentURL, upnp.iupnpservicedocumentaccess_getdocumenturl, upnp/IUPnPServiceDocumentAccess::GetDocumentURL
ms.topic: method
f1_keywords: 
 - "upnp/IUPnPServiceDocumentAccess.GetDocumentURL"
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUPnPServiceDocumentAccess.GetDocumentURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceDocumentAccess::GetDocumentURL


## -description


The <b>GetDocumentURL</b> method retrieves the Service Control Protocol Description (SCPD) URL for a service object. Using this URL, the UPnP control point can download the complete SCPD document.


## -parameters




### -param pbstrDocUrl [out]

The URL to the complete SCPD document.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns <b>E_FAIL</b>. This method will fail if called after a service enumeration has already started.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservicedocumentaccess">IUPnPServiceDocumentAccess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservicedocumentaccess-getdocument">IUPnPServiceDocumentAccess:GetDocument</a>
 

 

