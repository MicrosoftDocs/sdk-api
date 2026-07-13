---
UID: NF:wtsprotocol.IWRdsWddmIddProps.OnDriverUnload
title: IWRdsWddmIddProps::OnDriverUnload (wtsprotocol.h)
description: Termsrv uses this method to tell the protocol stack that PnP unloaded the WDDM ID driver.
helpviewer_keywords: ["IWRdsWddmIddProps interface [Remote Desktop Services]","OnDriverUnload method","IWRdsWddmIddProps.OnDriverUnload","IWRdsWddmIddProps::OnDriverUnload","OnDriverUnload","OnDriverUnload method [Remote Desktop Services]","OnDriverUnload method [Remote Desktop Services]","IWRdsWddmIddProps interface","termserv.iwrdswddmiddprops_ondriverunload","wtsprotocol/IWRdsWddmIddProps::OnDriverUnload"]
old-location: termserv\iwrdswddmiddprops_ondriverunload.htm
tech.root: TermServ
ms.assetid: D61C38FD-0298-4363-8A09-D0C2844C23CA
ms.date: 12/05/2018
ms.keywords: IWRdsWddmIddProps interface [Remote Desktop Services],OnDriverUnload method, IWRdsWddmIddProps.OnDriverUnload, IWRdsWddmIddProps::OnDriverUnload, OnDriverUnload, OnDriverUnload method [Remote Desktop Services], OnDriverUnload method [Remote Desktop Services],IWRdsWddmIddProps interface, termserv.iwrdswddmiddprops_ondriverunload, wtsprotocol/IWRdsWddmIddProps::OnDriverUnload
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
 - IWRdsWddmIddProps::OnDriverUnload
 - wtsprotocol/IWRdsWddmIddProps::OnDriverUnload
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
 - IWRdsWddmIddProps.OnDriverUnload
---

# IWRdsWddmIddProps::OnDriverUnload


## -description



Termsrv uses this method to tell the protocol stack that PnP unloaded the
    WDDM ID driver.

## -parameters

### -param SessionId [in]

ID of a session driver is unloaded from.

## -returns

Returns S_OK or error code

## -see-also

<a href="nn-wtsprotocol-iwrdswddmiddprops.md">IWRdsWddmIddProps</a>

