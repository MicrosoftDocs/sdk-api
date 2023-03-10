---
UID: NF:wsddisco.IWSDiscoveredService.GetProbeResolveTag
title: IWSDiscoveredService::GetProbeResolveTag (wsddisco.h)
description: Retrieves the search tag corresponding to this discovered service object.
helpviewer_keywords: ["GetProbeResolveTag","GetProbeResolveTag method","GetProbeResolveTag method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetProbeResolveTag method","IWSDiscoveredService.GetProbeResolveTag","IWSDiscoveredService::GetProbeResolveTag","ncd.iwsdiscoveredservice_getproberesolvetag","wsddisco/IWSDiscoveredService::GetProbeResolveTag"]
old-location: ncd\iwsdiscoveredservice_getproberesolvetag.htm
tech.root: ncd
ms.assetid: 80c22d39-0197-4e4d-b47e-e04ae90716f9
ms.date: 12/05/2018
ms.keywords: GetProbeResolveTag, GetProbeResolveTag method, GetProbeResolveTag method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetProbeResolveTag method, IWSDiscoveredService.GetProbeResolveTag, IWSDiscoveredService::GetProbeResolveTag, ncd.iwsdiscoveredservice_getproberesolvetag, wsddisco/IWSDiscoveredService::GetProbeResolveTag
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
 - IWSDiscoveredService::GetProbeResolveTag
 - wsddisco/IWSDiscoveredService::GetProbeResolveTag
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
 - IWSDiscoveredService.GetProbeResolveTag
---

# IWSDiscoveredService::GetProbeResolveTag


## -description

Retrieves the search tag corresponding to this discovered service object.

## -parameters

### -param ppszTag [out]

Search tag passed to the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a> search method that this <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object corresponds to. If the <b>IWSDiscoveredService</b> is the result of a Hello message, the tag is <b>NULL</b>. Do not deallocate the output string.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<i>ppszTag</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The resulting pointer value is only valid for the lifetime of the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>