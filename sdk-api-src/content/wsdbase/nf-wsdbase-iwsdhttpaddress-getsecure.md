---
UID: NF:wsdbase.IWSDHttpAddress.GetSecure
title: IWSDHttpAddress::GetSecure
author: windows-driver-content
description: Retrieves the status on whether TLS secure sessions are enabled for this address.
old-location: ncd\iwsdhttpaddress_getsecure.htm
old-project: WsdApi
ms.assetid: aaf9e918-7d1c-4457-94f8-888a99f07c18
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetSecure, GetSecure method, GetSecure method,IWSDHttpAddress interface, IWSDHttpAddress interface,GetSecure method, IWSDHttpAddress.GetSecure, IWSDHttpAddress::GetSecure, ncd.iwsdhttpaddress_getsecure, wsdbase/IWSDHttpAddress::GetSecure
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDHttpAddress.GetSecure
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpAddress::GetSecure


## -description


Retrieves the status on whether TLS secure sessions are enabled for this address.


## -parameters






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
TLS secure sessions are enabled for this address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
TLS secure sessions are disabled for this address.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a>
 

 

