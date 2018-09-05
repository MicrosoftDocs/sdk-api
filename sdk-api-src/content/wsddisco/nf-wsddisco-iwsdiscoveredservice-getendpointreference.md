---
UID: NF:wsddisco.IWSDiscoveredService.GetEndpointReference
title: IWSDiscoveredService::GetEndpointReference
author: windows-sdk-content
description: Retrieves a WS-Addressing address referencing an endpoint of the remote device.
old-location: ncd\iwsdiscoveredservice_getendpointreference.htm
old-project: WsdApi
ms.assetid: 656ff77d-765e-4c30-8e5d-560d121dc368
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetEndpointReference, GetEndpointReference method, GetEndpointReference method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetEndpointReference method, IWSDiscoveredService.GetEndpointReference, IWSDiscoveredService::GetEndpointReference, ncd.iwsdiscoveredservice_getendpointreference, wsddisco/IWSDiscoveredService::GetEndpointReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.redist: 
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveredService.GetEndpointReference
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveredService::GetEndpointReference


## -description


Retrieves a WS-Addressing address referencing an endpoint of the remote device.


## -parameters




### -param ppEndpointReference






#### - ppEndPointReference [out]

A WS-Addressing address referencing an endpoint of the remote device. For details, see <a href="https://msdn.microsoft.com/97d6870e-3633-4bea-9a50-984e6b0ba3a1">WSD_ENDPOINT_REFERENCE</a>. Do not deallocate the output structure.


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
<i>ppEndPointReference</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The resulting pointer value is only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

