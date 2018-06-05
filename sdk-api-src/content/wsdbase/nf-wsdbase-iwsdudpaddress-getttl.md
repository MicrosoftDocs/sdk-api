---
UID: NF:wsdbase.IWSDUdpAddress.GetTTL
title: IWSDUdpAddress::GetTTL
author: windows-sdk-content
description: Gets the time-to-live (TTL) for all outbound packets using this address.
old-location: ncd\iwsdudpaddress_getttl.htm
old-project: WsdApi
ms.assetid: 8bc2a973-a776-45c6-b6bf-cf268badab30
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetTTL, GetTTL method, GetTTL method,IWSDUdpAddress interface, IWSDUdpAddress interface,GetTTL method, IWSDUdpAddress.GetTTL, IWSDUdpAddress::GetTTL, ncd.iwsdudpaddress_getttl, wsdbase/IWSDUdpAddress::GetTTL
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDUdpAddress.GetTTL
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpAddress::GetTTL


## -description


Gets the time-to-live (TTL) for all outbound packets using this address.


## -parameters




### -param pdwTTL [out]

Pointer to the TTL of outgoing UDP packets. Generally, the TTL represents the maximum number of hops before a packet is discarded. Some implementations interpret the TTL differently. 


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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwTTL</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 

