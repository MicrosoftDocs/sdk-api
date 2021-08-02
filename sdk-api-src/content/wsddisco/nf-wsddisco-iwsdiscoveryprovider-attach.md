---
UID: NF:wsddisco.IWSDiscoveryProvider.Attach
title: IWSDiscoveryProvider::Attach (wsddisco.h)
description: Attaches a callback interface to the discovery provider.
helpviewer_keywords: ["Attach","Attach method","Attach method","IWSDiscoveryProvider interface","IWSDiscoveryProvider interface","Attach method","IWSDiscoveryProvider.Attach","IWSDiscoveryProvider::Attach","ncd.iwsdiscoveryprovider_attach_method","wsddisco/IWSDiscoveryProvider::Attach"]
old-location: ncd\iwsdiscoveryprovider_attach_method.htm
tech.root: ncd
ms.assetid: 3bb2aead-b082-4a2b-b4bf-97a1feb1e11e
ms.date: 12/05/2018
ms.keywords: Attach, Attach method, Attach method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,Attach method, IWSDiscoveryProvider.Attach, IWSDiscoveryProvider::Attach, ncd.iwsdiscoveryprovider_attach_method, wsddisco/IWSDiscoveryProvider::Attach
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
 - IWSDiscoveryProvider::Attach
 - wsddisco/IWSDiscoveryProvider::Attach
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
 - IWSDiscoveryProvider.Attach
---

# IWSDiscoveryProvider::Attach


## -description

Attaches a callback interface to the discovery provider.

## -parameters

### -param pSink [in]

Interface to receive callback notifications.  Search results as well as the Hello and Bye messages are communicated to this interface via the callbacks.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pSink</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has already been attached to the provider.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Attach must be called before any other <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> method is used, except for <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-setaddressfamily">SetAddressFamily</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>