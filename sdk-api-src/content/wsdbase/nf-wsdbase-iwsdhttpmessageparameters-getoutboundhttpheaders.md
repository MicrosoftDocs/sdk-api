---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetOutboundHttpHeaders
title: IWSDHttpMessageParameters::GetOutboundHttpHeaders (wsdbase.h)
author: windows-sdk-content
description: Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.
old-location: ncd\iwsdhttpmessageparameters_getoutboundhttpheaders.htm
tech.root: WsdApi
ms.assetid: c366773a-1869-4181-a457-560a1a9c84cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOutboundHttpHeaders, GetOutboundHttpHeaders method, GetOutboundHttpHeaders method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetOutboundHttpHeaders method, IWSDHttpMessageParameters.GetOutboundHttpHeaders, IWSDHttpMessageParameters::GetOutboundHttpHeaders, ncd.iwsdhttpmessageparameters_getoutboundhttpheaders, wsdbase/IWSDHttpMessageParameters::GetOutboundHttpHeaders
ms.topic: method
f1_keywords: 
 - "wsdbase/IWSDHttpMessageParameters.GetOutboundHttpHeaders"
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
 - IWSDHttpMessageParameters.GetOutboundHttpHeaders
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>
 

 

