---
UID: NF:wsddisco.IWSDiscoveredService.GetProbeResolveTag
title: IWSDiscoveredService::GetProbeResolveTag
author: windows-sdk-content
description: Retrieves the search tag corresponding to this discovered service object.
old-location: ncd\iwsdiscoveredservice_getproberesolvetag.htm
tech.root: wsdapi
ms.assetid: 80c22d39-0197-4e4d-b47e-e04ae90716f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetProbeResolveTag, GetProbeResolveTag method, GetProbeResolveTag method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetProbeResolveTag method, IWSDiscoveredService.GetProbeResolveTag, IWSDiscoveredService::GetProbeResolveTag, ncd.iwsdiscoveredservice_getproberesolvetag, wsddisco/IWSDiscoveredService::GetProbeResolveTag
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
 - IWSDiscoveredService.GetProbeResolveTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveredService::GetProbeResolveTag


## -description


Retrieves the search tag corresponding to this discovered service object. 


## -parameters




### -param ppszTag [out]

Search tag passed to the <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a> search method that this <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object corresponds to. If the <b>IWSDiscoveredService</b> is the result of a Hello message, the tag is <b>NULL</b>. Do not deallocate the output string. 


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



The resulting pointer value is only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

