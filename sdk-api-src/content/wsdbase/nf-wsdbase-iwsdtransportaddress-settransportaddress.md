---
UID: NF:wsdbase.IWSDTransportAddress.SetTransportAddress
title: IWSDTransportAddress::SetTransportAddress
author: windows-sdk-content
description: Sets the string representation of the transport address.
old-location: ncd\iwsdtransportaddress_settransportaddress.htm
tech.root: WsdApi
ms.assetid: ea87b7d8-71c0-4cb6-b28b-7ac8f2417886
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDTransportAddress interface,SetTransportAddress method, IWSDTransportAddress.SetTransportAddress, IWSDTransportAddress::SetTransportAddress, SetTransportAddress, SetTransportAddress method, SetTransportAddress method,IWSDTransportAddress interface, ncd.iwsdtransportaddress_settransportaddress, wsdbase/IWSDTransportAddress::SetTransportAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDTransportAddress.SetTransportAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDTransportAddress::SetTransportAddress


## -description


Sets the string representation of the transport address.  The format of the string varies, and is determined by the implementing interface (either <a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a> or <a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>).


## -parameters




### -param pszAddress [in]

String representation of the transport address. 


## -returns



This method can return one of these values.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of the address string pointed to by <i>ppszAddress</i> exceeds WSD_MAX_TEXT_LENGTH (8192),  <i>ppszAddress</i> is <b>NULL</b>, or the format of <i>ppszAddress</i> was not recognized. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>
 

 

