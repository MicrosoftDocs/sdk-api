---
UID: NN:upnp.IUPnPServiceDocumentAccess
title: IUPnPServiceDocumentAccess
author: windows-sdk-content
description: Use this interface to retrieve and provide the Service Control Protocol Description (SCPD) document to a UPnP control point application to expose actions supported by the service and provide information about state variables.
old-location: upnp\iupnpservicedocumentaccess.htm
old-project: UPnP
ms.assetid: A4890300-2945-4973-ACFC-F950C5E15A0E
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: IUPnPServiceDocumentAccess, IUPnPServiceDocumentAccess interface [UPnP APIs], IUPnPServiceDocumentAccess interface [UPnP APIs],described, upnp.iupnpservicedocumentaccess, upnp/IUPnPServiceDocumentAccess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnp.dll
api_name:
-	IUPnPServiceDocumentAccess
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceDocumentAccess interface


## -description


 Use this interface to retrieve and provide the Service Control Protocol Description (SCPD) document to a UPnP control point application to expose actions supported by the service and provide information about state variables.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceDocumentAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUPnPServiceDocumentAccess</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B0C197A0-4987-43BD-A48D-BF2E6150A85F">GetDocument</a>
</td>
<td align="left" width="63%">
Retrieves the complete SCPD document for a service object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57AF4510-89D6-4DD5-B164-1478A5C27E20">GetDocumentURL</a>
</td>
<td align="left" width="63%">
Retrieves the SCPD URL for a service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>
 

 

