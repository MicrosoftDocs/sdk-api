---
UID: NF:wsddisco.IWSDiscoveredService.GetScopes
title: IWSDiscoveredService::GetScopes (wsddisco.h)
author: windows-sdk-content
description: Retrieves a list of WS-Discovery Scopes.
old-location: ncd\iwsdiscoveredservice_getscopes.htm
tech.root: WsdApi
ms.assetid: 9b389ba3-9cc1-4bc2-949a-e7103378cbcc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetScopes, GetScopes method, GetScopes method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetScopes method, IWSDiscoveredService.GetScopes, IWSDiscoveredService::GetScopes, ncd.iwsdiscoveredservice_getscopes, wsddisco/IWSDiscoveredService::GetScopes
ms.topic: method
f1_keywords:
- wsddisco/IWSDiscoveredService.GetScopes
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsdapi.dll
api_name:
- IWSDiscoveredService.GetScopes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveredService::GetScopes


## -description


Retrieves a list of WS-Discovery Scopes.


## -parameters




### -param ppScopesList [out]

List of WS-Discovery Scopes provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device. For details, see <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_uri_list">WSD_URI_LIST</a>. Do not deallocate the output structure.


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
<i>ppScopesList</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The resulting pointer value is only valid for the lifetime of the <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>
 

 

