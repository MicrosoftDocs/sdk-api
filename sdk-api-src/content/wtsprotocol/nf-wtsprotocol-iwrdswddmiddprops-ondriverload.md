---
UID: NF:wtsprotocol.IWRdsWddmIddProps.OnDriverLoad
title: IWRdsWddmIddProps::OnDriverLoad
author: windows-sdk-content
description: Termsrv uses this method to return a handle of the loaded WDDM ID driver to the protocol stack. From this point the stack owns the handle and needs to call CloseHandle() after communication with the driver is no longer needed.
old-location: termserv\iwrdswddmiddprops_ondriverload.htm
tech.root: termserv
ms.assetid: 8070441A-60E1-4752-A987-A5BD322AA55A
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWRdsWddmIddProps interface [Remote Desktop Services],OnDriverLoad method, IWRdsWddmIddProps.OnDriverLoad, IWRdsWddmIddProps::OnDriverLoad, OnDriverLoad, OnDriverLoad method [Remote Desktop Services], OnDriverLoad method [Remote Desktop Services],IWRdsWddmIddProps interface, termserv.iwrdswddmiddprops_ondriverload, wtsprotocol/IWRdsWddmIddProps::OnDriverLoad
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWRdsWddmIddProps.OnDriverLoad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wtsprotocol.h
: 
- IWRdsWddmIddProps.OnDriverLoad
: 
---

# IWRdsWddmIddProps::OnDriverLoad


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Termsrv uses this method to return a handle of the loaded WDDM ID driver to 
    the protocol stack. From this point the stack owns the handle and needs to call 
    CloseHandle() after communication with the driver is no longer needed.


## -parameters




### -param SessionId [in]

ID of the session that the driver is loaded for.


### -param DriverHandle [in]

Opened handle of the WDDM ID driver.


## -returns



S_OK or error code




## -see-also




<a href="https://msdn.microsoft.com/9473E754-D158-40E7-9E76-D8EA5A4BE86E">IWRdsWddmIddProps</a>
 

 

