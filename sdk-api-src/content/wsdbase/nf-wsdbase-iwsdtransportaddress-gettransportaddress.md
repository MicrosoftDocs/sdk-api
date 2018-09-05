---
UID: NF:wsdbase.IWSDTransportAddress.GetTransportAddress
title: IWSDTransportAddress::GetTransportAddress
author: windows-sdk-content
description: Gets a pointer to a string representation of the address object.
old-location: ncd\iwsdtransportaddress_gettransportaddress.htm
old-project: WsdApi
ms.assetid: 090b009d-0cca-4925-bf90-cb3d0975d271
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetTransportAddress, GetTransportAddress method, GetTransportAddress method,IWSDTransportAddress interface, IWSDTransportAddress interface,GetTransportAddress method, IWSDTransportAddress.GetTransportAddress, IWSDTransportAddress::GetTransportAddress, ncd.iwsdtransportaddress_gettransportaddress, wsdbase/IWSDTransportAddress::GetTransportAddress
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
 - wsdapi.dll
api_name:
 - IWSDTransportAddress.GetTransportAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDTransportAddress::GetTransportAddress


## -description


Gets a pointer to a string representation of the address object.  The format of the string varies, and is determined by the implementing interface (either <a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a> or <a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>).


## -parameters




### -param ppszAddress [out]

String representation of the address object. Do not deallocate this pointer.


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
<i>ppszAddress</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The transport address has not yet been set. To set the transport address, call <a href="https://msdn.microsoft.com/ea87b7d8-71c0-4cb6-b28b-7ac8f2417886">SetTransportAddress</a> with a non-<b>NULL</b> address.

</td>
</tr>
</table>
 




## -remarks



The string returned by this method may contain an IPv4 or unbracketed IPv6 address such as "fe80::1".  It may also contain a bracketed IPv6 address that includes the port such as "[fe80::1]:1234".  The caller should parse the string carefully to account for both possibilities. 




## -see-also




<a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>
 

 

