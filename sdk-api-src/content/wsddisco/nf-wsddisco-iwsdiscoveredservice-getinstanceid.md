---
UID: NF:wsddisco.IWSDiscoveredService.GetInstanceId
title: IWSDiscoveredService::GetInstanceId (wsddisco.h)
description: Retrieves the instance identifier of this message.
helpviewer_keywords: ["GetInstanceId","GetInstanceId method","GetInstanceId method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetInstanceId method","IWSDiscoveredService.GetInstanceId","IWSDiscoveredService::GetInstanceId","ncd.iwsdiscoveredservice_getinstanceid","wsddisco/IWSDiscoveredService::GetInstanceId"]
old-location: ncd\iwsdiscoveredservice_getinstanceid.htm
tech.root: ncd
ms.assetid: 993f4ef1-ff13-4454-b22f-29c9628da5e0
ms.date: 12/05/2018
ms.keywords: GetInstanceId, GetInstanceId method, GetInstanceId method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetInstanceId method, IWSDiscoveredService.GetInstanceId, IWSDiscoveredService::GetInstanceId, ncd.iwsdiscoveredservice_getinstanceid, wsddisco/IWSDiscoveredService::GetInstanceId
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
 - IWSDiscoveredService::GetInstanceId
 - wsddisco/IWSDiscoveredService::GetInstanceId
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
 - IWSDiscoveredService.GetInstanceId
---

# IWSDiscoveredService::GetInstanceId


## -description

Retrieves the instance identifier of this message.

## -parameters

### -param pullInstanceId [out]

A pointer to the instance identifier of this message.

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
<i>pullInstanceId</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>