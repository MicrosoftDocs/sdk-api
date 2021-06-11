---
UID: NF:wtsprotocol.IWRdsWddmIddProps.OnDriverLoad
title: IWRdsWddmIddProps::OnDriverLoad (wtsprotocol.h)
description: Termsrv uses this method to return a handle of the loaded WDDM ID driver to the protocol stack. From this point the stack owns the handle and needs to call CloseHandle() after communication with the driver is no longer needed.
helpviewer_keywords: ["IWRdsWddmIddProps interface [Remote Desktop Services]","OnDriverLoad method","IWRdsWddmIddProps.OnDriverLoad","IWRdsWddmIddProps::OnDriverLoad","OnDriverLoad","OnDriverLoad method [Remote Desktop Services]","OnDriverLoad method [Remote Desktop Services]","IWRdsWddmIddProps interface","termserv.iwrdswddmiddprops_ondriverload","wtsprotocol/IWRdsWddmIddProps::OnDriverLoad"]
old-location: termserv\iwrdswddmiddprops_ondriverload.htm
tech.root: TermServ
ms.assetid: 8070441A-60E1-4752-A987-A5BD322AA55A
ms.date: 12/05/2018
ms.keywords: IWRdsWddmIddProps interface [Remote Desktop Services],OnDriverLoad method, IWRdsWddmIddProps.OnDriverLoad, IWRdsWddmIddProps::OnDriverLoad, OnDriverLoad, OnDriverLoad method [Remote Desktop Services], OnDriverLoad method [Remote Desktop Services],IWRdsWddmIddProps interface, termserv.iwrdswddmiddprops_ondriverload, wtsprotocol/IWRdsWddmIddProps::OnDriverLoad
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsWddmIddProps::OnDriverLoad
 - wtsprotocol/IWRdsWddmIddProps::OnDriverLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWRdsWddmIddProps.OnDriverLoad
---

# IWRdsWddmIddProps::OnDriverLoad


## -description



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

<a href="nn-wtsprotocol-iwrdswddmiddprops.md">IWRdsWddmIddProps</a>

