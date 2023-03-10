---
UID: NN:wsddisco.IWSDiscoveredService
title: IWSDiscoveredService (wsddisco.h)
description: This interface represents a remotely discovered host.
helpviewer_keywords: ["IWSDiscoveredService","IWSDiscoveredService interface","IWSDiscoveredService interface","described","ncd.iwsdiscoveredservice","wsddisco/IWSDiscoveredService"]
old-location: ncd\iwsdiscoveredservice.htm
tech.root: ncd
ms.assetid: 6516098a-e440-4dec-b275-165ea3072d49
ms.date: 12/05/2018
ms.keywords: IWSDiscoveredService, IWSDiscoveredService interface, IWSDiscoveredService interface,described, ncd.iwsdiscoveredservice, wsddisco/IWSDiscoveredService
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
 - IWSDiscoveredService
 - wsddisco/IWSDiscoveredService
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
 - IWSDiscoveredService
---

# IWSDiscoveredService interface


## -description

This interface represents a remotely discovered host.  WSDAPI returns this interface when calling  <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-add">IWSDiscoveryProviderNotify::Add</a> and <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovidernotify-remove">IWSDiscoveryProviderNotify::Remove</a>. The interface is populated when a match for an outstanding query issued using <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype">IWSDiscoveryProvider::SearchByType</a>, <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress">IWSDiscoveryProvider::SearchByAddress</a>, or <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid">IWSDiscoveryProvider::SearchById</a> is received, or if a device on the network announces itself with a Hello message.

## -inheritance

The <b>IWSDiscoveredService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveredService</b> also has these types of members:

