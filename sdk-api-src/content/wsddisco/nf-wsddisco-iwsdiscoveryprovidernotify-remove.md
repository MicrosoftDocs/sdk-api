---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.Remove
title: IWSDiscoveryProviderNotify::Remove (wsddisco.h)
description: Provides information on a recently departed discovery host (from a Bye message).
helpviewer_keywords: ["IWSDiscoveryProviderNotify interface","Remove method","IWSDiscoveryProviderNotify.Remove","IWSDiscoveryProviderNotify::Remove","Remove","Remove method","Remove method","IWSDiscoveryProviderNotify interface","ncd.iwsdiscoveryprovidernotify_remove","wsddisco/IWSDiscoveryProviderNotify::Remove"]
old-location: ncd\iwsdiscoveryprovidernotify_remove.htm
tech.root: ncd
ms.assetid: 776fc1d5-9dfe-445f-9af6-36faf971bf37
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProviderNotify interface,Remove method, IWSDiscoveryProviderNotify.Remove, IWSDiscoveryProviderNotify::Remove, Remove, Remove method, Remove method,IWSDiscoveryProviderNotify interface, ncd.iwsdiscoveryprovidernotify_remove, wsddisco/IWSDiscoveryProviderNotify::Remove
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveryProviderNotify::Remove
 - wsddisco/IWSDiscoveryProviderNotify::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProviderNotify.Remove
---

# IWSDiscoveryProviderNotify::Remove


## -description

Provides information on a recently departed discovery host (from a Bye message).

## -parameters

### -param pService [in]

A pointer to an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> interface that represents a remote discovery host.

## -returns

The return value is not meaningful. An implementer should return S_OK.

## -remarks

<b>Remove</b> will be called once per announcement of a departing discovery host.

<div class="alert"><b>Note</b>  Multiple simultaneous calls may be made to <b>Remove</b> by the provider, so it is essential that shared data be synchronized when implementing this callback routine.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovidernotify">IWSDiscoveryProviderNotify</a>