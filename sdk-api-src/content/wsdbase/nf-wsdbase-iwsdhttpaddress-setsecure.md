---
UID: NF:wsdbase.IWSDHttpAddress.SetSecure
title: IWSDHttpAddress::SetSecure
author: windows-driver-content
description: Enables or disables TLS secure sessions for this address.
old-location: ncd\iwsdhttpaddress_setsecure.htm
old-project: WsdApi
ms.assetid: f2b66d0d-51b2-437e-8ceb-a4c95f2f9d6d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDHttpAddress interface,SetSecure method, IWSDHttpAddress.SetSecure, IWSDHttpAddress::SetSecure, SetSecure, SetSecure method, SetSecure method,IWSDHttpAddress interface, ncd.iwsdhttpaddress_setsecure, wsdbase/IWSDHttpAddress::SetSecure
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
-	IWSDHttpAddress.SetSecure
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpAddress::SetSecure


## -description


Enables or disables TLS secure sessions for this address.


## -parameters




### -param fSecure [in]

<b>TRUE</b> to enable TLS secure session communications for this address, <b>FALSE</b> to disable TLS.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/79d3570a-56b2-40ad-b3c6-cddc3239da7e">IWSDHttpAddress</a>
 

 

