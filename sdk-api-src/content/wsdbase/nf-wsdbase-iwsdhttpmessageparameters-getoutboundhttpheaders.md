---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetOutboundHttpHeaders
title: IWSDHttpMessageParameters::GetOutboundHttpHeaders
author: windows-driver-content
description: Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.
old-location: ncd\iwsdhttpmessageparameters_getoutboundhttpheaders.htm
old-project: WsdApi
ms.assetid: c366773a-1869-4181-a457-560a1a9c84cd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetOutboundHttpHeaders, GetOutboundHttpHeaders method, GetOutboundHttpHeaders method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetOutboundHttpHeaders method, IWSDHttpMessageParameters.GetOutboundHttpHeaders, IWSDHttpMessageParameters::GetOutboundHttpHeaders, ncd.iwsdhttpmessageparameters_getoutboundhttpheaders, wsdbase/IWSDHttpMessageParameters::GetOutboundHttpHeaders
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
-	IWSDHttpMessageParameters.GetOutboundHttpHeaders
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpMessageParameters::GetOutboundHttpHeaders


## -description


Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.


## -parameters




### -param ppszHeaders [out]

Pointer used to receive the current HTTP headers in use.  Do not deallocate this pointer.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppszHeaders</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There are no headers available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>
 

 

