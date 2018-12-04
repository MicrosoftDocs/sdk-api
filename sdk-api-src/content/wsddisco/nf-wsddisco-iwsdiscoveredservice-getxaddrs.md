---
UID: NF:wsddisco.IWSDiscoveredService.GetXAddrs
title: IWSDiscoveredService::GetXAddrs
author: windows-sdk-content
description: Retrieves a list of WS-Discovery XAddrs.
old-location: ncd\iwsdiscoveredservice_getxaddrs.htm
tech.root: wsdapi
ms.assetid: a861374e-fee4-486b-8e23-f4a4a8203b28
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetXAddrs, GetXAddrs method, GetXAddrs method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetXAddrs method, IWSDiscoveredService.GetXAddrs, IWSDiscoveredService::GetXAddrs, ncd.iwsdiscoveredservice_getxaddrs, wsddisco/IWSDiscoveredService::GetXAddrs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWSDiscoveredService.GetXAddrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveredService::GetXAddrs


## -description


Retrieves a list of WS-Discovery XAddrs.


## -parameters




### -param ppXAddrsList [out]

List of WS-Discovery XAddrs provided in the Hello, ProbeMatch, or ResolveMatch message sent by the remote device. For details, see <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a>. Do not deallocate the output structure.


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
<i>ppXAddrsList</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The resulting pointer value is only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

