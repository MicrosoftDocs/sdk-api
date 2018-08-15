---
UID: NF:wsddisco.IWSDiscoveredService.GetRemoteTransportAddress
title: IWSDiscoveredService::GetRemoteTransportAddress
author: windows-sdk-content
description: Retrieves the string representation of the remote transport (IP) address.
old-location: ncd\iwsdiscoveredservice_getremotetransportaddress.htm
old-project: wsdapi
ms.assetid: 15376e12-fd7c-4cf5-a950-bf492392afa3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetRemoteTransportAddress, GetRemoteTransportAddress method, GetRemoteTransportAddress method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetRemoteTransportAddress method, IWSDiscoveredService.GetRemoteTransportAddress, IWSDiscoveredService::GetRemoteTransportAddress, ncd.iwsdiscoveredservice_getremotetransportaddress, wsddisco/IWSDiscoveredService::GetRemoteTransportAddress
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
 - IWSDiscoveredService.GetRemoteTransportAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveredService::GetRemoteTransportAddress


## -description


Retrieves the string representation of the remote transport (IP) address.



## -parameters




### -param ppszRemoteTransportAddress [out]

String representation of the remote transport (IP) address. Is <b>NULL</b> if not available.
Do not deallocate the output string.


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
<i>ppszRemoteTransportAddress</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The resulting pointer value is only valid for the lifetime of the <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> object.

The string returned by this method may contain an IPv4 or unbracketed IPv6 address such as "fe80::1".  It may also contain a bracketed IPv6 address that includes the port such as "[fe80::1]:1234".  The caller should parse the string carefully to account for both possibilities. 




## -see-also




<a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>
 

 

