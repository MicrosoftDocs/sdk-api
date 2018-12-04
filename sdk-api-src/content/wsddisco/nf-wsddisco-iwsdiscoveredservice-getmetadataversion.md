---
UID: NF:wsddisco.IWSDiscoveredService.GetMetadataVersion
title: IWSDiscoveredService::GetMetadataVersion
author: windows-sdk-content
description: Retrieves the metadata version of this message.
old-location: ncd\iwsdiscoveredservice_getmetadataversion.htm
tech.root: wsdapi
ms.assetid: ce0d463e-6455-48cc-b01f-6aa93fd628b6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetMetadataVersion, GetMetadataVersion method, GetMetadataVersion method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetMetadataVersion method, IWSDiscoveredService.GetMetadataVersion, IWSDiscoveredService::GetMetadataVersion, ncd.iwsdiscoveredservice_getmetadataversion, wsddisco/IWSDiscoveredService::GetMetadataVersion
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
 - IWSDiscoveredService.GetMetadataVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveredService::GetMetadataVersion


## -description


Retrieves the metadata version of this message.


## -parameters




### -param pullMetadataVersion [out]

Metadata version of this message.


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
<i>pullMetadataVersion</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Versioning is used to determine if metadata exchange should be performed again due to a state change on the device.




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

