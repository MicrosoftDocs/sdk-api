---
UID: NF:wsdbase.IWSDTransportAddress.GetPort
title: IWSDTransportAddress::GetPort
author: windows-sdk-content
description: Gets the IP port number associated with this transport address.
old-location: ncd\iwsdtransportaddress_getport.htm
old-project: WsdApi
ms.assetid: cc2e623f-e6b6-42ad-b0de-7960de0142d0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetPort, GetPort method, GetPort method,IWSDTransportAddress interface, IWSDTransportAddress interface,GetPort method, IWSDTransportAddress.GetPort, IWSDTransportAddress::GetPort, ncd.iwsdtransportaddress_getport, wsdbase/IWSDTransportAddress::GetPort
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
 - IWSDTransportAddress.GetPort
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDTransportAddress::GetPort


## -description


Gets the IP port number associated with this transport address.


## -parameters




### -param pwPort [out]

Port number associated with the address object.


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
<i>pwPort</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a>
 

 

