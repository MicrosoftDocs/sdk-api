---
UID: NF:wsddisco.IWSDiscoveredService.GetLocalInterfaceGUID
title: IWSDiscoveredService::GetLocalInterfaceGUID (wsddisco.h)
description: Retrieves the GUID of the local network interface over which the message was received.
helpviewer_keywords: ["GetLocalInterfaceGUID","GetLocalInterfaceGUID method","GetLocalInterfaceGUID method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetLocalInterfaceGUID method","IWSDiscoveredService.GetLocalInterfaceGUID","IWSDiscoveredService::GetLocalInterfaceGUID","ncd.iwsdiscoveredservice_getlocalinterfaceguid","wsddisco/IWSDiscoveredService::GetLocalInterfaceGUID"]
old-location: ncd\iwsdiscoveredservice_getlocalinterfaceguid.htm
tech.root: ncd
ms.assetid: 9c66bda4-d21c-443f-a9b0-e05485306bde
ms.date: 12/05/2018
ms.keywords: GetLocalInterfaceGUID, GetLocalInterfaceGUID method, GetLocalInterfaceGUID method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetLocalInterfaceGUID method, IWSDiscoveredService.GetLocalInterfaceGUID, IWSDiscoveredService::GetLocalInterfaceGUID, ncd.iwsdiscoveredservice_getlocalinterfaceguid, wsddisco/IWSDiscoveredService::GetLocalInterfaceGUID
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
 - IWSDiscoveredService::GetLocalInterfaceGUID
 - wsddisco/IWSDiscoveredService::GetLocalInterfaceGUID
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
 - IWSDiscoveredService.GetLocalInterfaceGUID
---

# IWSDiscoveredService::GetLocalInterfaceGUID


## -description

Retrieves the GUID of the local network interface over which the message was received.

## -parameters

### -param pGuid [out]

GUID of the local network interface over which the message was received. Structure will be cleared if the local interface GUID is not available.

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
<i>pGuid</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>