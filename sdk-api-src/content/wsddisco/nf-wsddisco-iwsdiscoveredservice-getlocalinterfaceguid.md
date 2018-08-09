---
UID: NF:wsddisco.IWSDiscoveredService.GetLocalInterfaceGUID
title: IWSDiscoveredService::GetLocalInterfaceGUID
author: windows-sdk-content
description: Retrieves the GUID of the local network interface over which the message was received.
old-location: ncd\iwsdiscoveredservice_getlocalinterfaceguid.htm
old-project: wsdapi
ms.assetid: 9c66bda4-d21c-443f-a9b0-e05485306bde
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetLocalInterfaceGUID, GetLocalInterfaceGUID method, GetLocalInterfaceGUID method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetLocalInterfaceGUID method, IWSDiscoveredService.GetLocalInterfaceGUID, IWSDiscoveredService::GetLocalInterfaceGUID, ncd.iwsdiscoveredservice_getlocalinterfaceguid, wsddisco/IWSDiscoveredService::GetLocalInterfaceGUID
ms.prod: windows
ms.technology: windows-sdk
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
 - IWSDiscoveredService.GetLocalInterfaceGUID
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

