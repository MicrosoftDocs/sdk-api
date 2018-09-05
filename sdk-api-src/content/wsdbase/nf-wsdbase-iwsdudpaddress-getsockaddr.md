---
UID: NF:wsdbase.IWSDUdpAddress.GetSockaddr
title: IWSDUdpAddress::GetSockaddr
author: windows-sdk-content
description: Gets the socket address information.
old-location: ncd\iwsdudpaddress_getsockaddr.htm
old-project: WsdApi
ms.assetid: 4a29722f-a3b7-4285-9ade-06de125f8b91
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSockaddr, GetSockaddr method, GetSockaddr method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetSockaddr method, IWSDUdpAddress.GetSockaddr, IWSDUdpAddress::GetSockaddr, ncd.iwsdudpaddress_getsockaddr, wsdbase/IWSDUdpAddress::GetSockaddr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.GetSockaddr
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpAddress::GetSockaddr


## -description


Gets the socket address information.


## -parameters




### -param pSockAddr [out]

Pointer to a <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure that contains the address information.


## -returns



Possible return values include, but are not limited to, the following:

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
<i>pSockAddr</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

