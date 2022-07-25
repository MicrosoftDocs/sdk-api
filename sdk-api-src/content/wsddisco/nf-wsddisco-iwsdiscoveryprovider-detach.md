---
UID: NF:wsddisco.IWSDiscoveryProvider.Detach
title: IWSDiscoveryProvider::Detach (wsddisco.h)
description: Detaches a callback interface from the discovery provider.
helpviewer_keywords: ["Detach","Detach method","Detach method","IWSDiscoveryProvider interface","IWSDiscoveryProvider interface","Detach method","IWSDiscoveryProvider.Detach","IWSDiscoveryProvider::Detach","ncd.iwsdiscoveryprovider_detach_method","wsddisco/IWSDiscoveryProvider::Detach"]
old-location: ncd\iwsdiscoveryprovider_detach_method.htm
tech.root: ncd
ms.assetid: 562e7618-06ac-4bd3-9746-6ff3a7531b6b
ms.date: 12/05/2018
ms.keywords: Detach, Detach method, Detach method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,Detach method, IWSDiscoveryProvider.Detach, IWSDiscoveryProvider::Detach, ncd.iwsdiscoveryprovider_detach_method, wsddisco/IWSDiscoveryProvider::Detach
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
 - IWSDiscoveryProvider::Detach
 - wsddisco/IWSDiscoveryProvider::Detach
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
 - IWSDiscoveryProvider.Detach
---

# IWSDiscoveryProvider::Detach


## -description

Detaches a callback interface from the discovery provider.



## -returns

Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has not been attached. You must call <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a> before calling this method.

</td>
</tr>
</table>

## -remarks

If a callback interface has been attached to a discovery provider via the <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a> method, then <b>Detach</b> must be called before releasing the reference to the provider interface object.

The <b>Detach</b> operation blocks until all callbacks into the associated <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovidernotify">IWSDiscoveryProviderNotify</a> object have completed.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>
