---
UID: NN:upnp.IUPnPServiceDocumentAccess
title: IUPnPServiceDocumentAccess (upnp.h)
author: windows-sdk-content
description: Use this interface to retrieve and provide the Service Control Protocol Description (SCPD) document to a UPnP control point application to expose actions supported by the service and provide information about state variables.
old-location: upnp\iupnpservicedocumentaccess.htm
tech.root: upnp
ms.assetid: A4890300-2945-4973-ACFC-F950C5E15A0E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPServiceDocumentAccess, IUPnPServiceDocumentAccess interface [UPnP APIs], IUPnPServiceDocumentAccess interface [UPnP APIs],described, upnp.iupnpservicedocumentaccess, upnp/IUPnPServiceDocumentAccess
ms.topic: interface
f1_keywords: ["upnp/IUPnPServiceDocumentAccess"]
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
 - IUPnPServiceDocumentAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceDocumentAccess interface


## -description


 Use this interface to retrieve and provide the Service Control Protocol Description (SCPD) document to a UPnP control point application to expose actions supported by the service and provide information about state variables.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceDocumentAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceDocumentAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceDocumentAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservicedocumentaccess-getdocument">GetDocument</a>
</td>
<td align="left" width="63%">
Retrieves the complete SCPD document for a service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservicedocumentaccess-getdocumenturl">GetDocumentURL</a>
</td>
<td align="left" width="63%">
Retrieves the SCPD URL for a service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>
 

 

