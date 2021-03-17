---
UID: NF:wsddisco.IWSDiscoveredService.GetTypes
title: IWSDiscoveredService::GetTypes (wsddisco.h)
description: Retrieves a list of WS-Discovery Types.
helpviewer_keywords: ["GetTypes","GetTypes method","GetTypes method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetTypes method","IWSDiscoveredService.GetTypes","IWSDiscoveredService::GetTypes","ncd.iwsdiscoveredservice_gettypes","wsddisco/IWSDiscoveredService::GetTypes"]
old-location: ncd\iwsdiscoveredservice_gettypes.htm
tech.root: ncd
ms.assetid: fda4def4-4c1d-49a7-bfc1-56ff744a7a9d
ms.date: 12/05/2018
ms.keywords: GetTypes, GetTypes method, GetTypes method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetTypes method, IWSDiscoveredService.GetTypes, IWSDiscoveredService::GetTypes, ncd.iwsdiscoveredservice_gettypes, wsddisco/IWSDiscoveredService::GetTypes
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
 - IWSDiscoveredService::GetTypes
 - wsddisco/IWSDiscoveredService::GetTypes
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
 - IWSDiscoveredService.GetTypes
---

# IWSDiscoveredService::GetTypes


## -description

Retrieves a list of WS-Discovery Types.

## -parameters

### -param ppTypesList [in]

List of WS-Discovery Types provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device. For details, see <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_name_list">WSD_NAME_LIST</a>. Do not deallocate the output structure.

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
<i>ppTypesList</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The resulting pointer value is only valid for the lifetime of the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>