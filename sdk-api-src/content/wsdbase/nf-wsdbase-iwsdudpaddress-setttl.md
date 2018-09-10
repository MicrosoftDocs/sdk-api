---
UID: NF:wsdbase.IWSDUdpAddress.SetTTL
title: IWSDUdpAddress::SetTTL
author: windows-sdk-content
description: Sets the time-to-live (TTL) for all outbound packets using this address.
old-location: ncd\iwsdudpaddress_setttl.htm
tech.root: WsdApi
ms.assetid: 3fcd8dd1-a00c-4085-a608-cb680285d869
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDUdpAddress interface,SetTTL method, IWSDUdpAddress.SetTTL, IWSDUdpAddress::SetTTL, SetTTL, SetTTL method, SetTTL method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setttl, wsdbase/IWSDUdpAddress::SetTTL
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
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.SetTTL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDUdpAddress::SetTTL


## -description


Sets the time-to-live (TTL) for all outbound packets using this address.


## -parameters




### -param dwTTL [in]

The TTL of outgoing UDP packets. Generally, the TTL represents the maximum number of hops before a packet is discarded. Some implementations interpret the TTL differently. 


## -returns



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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwTTL</i> is greater than 255.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

