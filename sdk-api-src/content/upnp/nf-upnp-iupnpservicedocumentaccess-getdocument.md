---
UID: NF:upnp.IUPnPServiceDocumentAccess.GetDocument
title: IUPnPServiceDocumentAccess::GetDocument method
author: windows-driver-content
description: GetDocument method retrieves the Service Control Protocol Description (SCPD) document for a service object.
old-location: upnp\iupnpservicedocumentaccess_getdocument.htm
old-project: UPnP
ms.assetid: B0C197A0-4987-43BD-A48D-BF2E6150A85F
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetDocument method [UPnP APIs], GetDocument method [UPnP APIs], IUPnPServiceDocumentAccess interface, GetDocument,IUPnPServiceDocumentAccess.GetDocument, IUPnPServiceDocumentAccess, IUPnPServiceDocumentAccess interface [UPnP APIs], GetDocument method, IUPnPServiceDocumentAccess::GetDocument, upnp.iupnpservicedocumentaccess_getdocument, upnp/IUPnPServiceDocumentAccess::GetDocument
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnp.dll
api_name:
-	IUPnPServiceDocumentAccess.GetDocument
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPServiceDocumentAccess::GetDocument method


## -description


The <b>GetDocument</b> method retrieves the Service Control Protocol Description (SCPD) document for a service object. The information provided by this document enables the user to pre-determine which actions are supported by the service, or review information about state variables.


## -parameters




### -param pbstrDoc [out]

The  complete SCPD document.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/A4890300-2945-4973-ACFC-F950C5E15A0E">IUPnPServiceDocumentAccess</a>



<a href="https://msdn.microsoft.com/57AF4510-89D6-4DD5-B164-1478A5C27E20">IUPnPServiceDocumentAccess::GetDocumentURL</a>
 

 

