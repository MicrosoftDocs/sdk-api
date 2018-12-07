---
UID: NF:wsdclient.IWSDEndpointProxy.GetErrorInfo
title: IWSDEndpointProxy::GetErrorInfo
author: windows-sdk-content
description: Retrieves information on the last error.
old-location: ncd\iwsdendpointproxy_geterrorinfo.htm
tech.root: wsdapi
ms.assetid: 950f5634-1cc5-4981-9053-e9090374cc5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetErrorInfo, GetErrorInfo method, GetErrorInfo method,IWSDEndpointProxy interface, IWSDEndpointProxy interface,GetErrorInfo method, IWSDEndpointProxy.GetErrorInfo, IWSDEndpointProxy::GetErrorInfo, ncd.iwsdendpointproxy_geterrorinfo, wsdclient/IWSDEndpointProxy::GetErrorInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDEndpointProxy.GetErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy::GetErrorInfo


## -description


Retrieves information on the last error.


## -parameters




### -param ppszErrorInfo [out]

Pointer to a buffer containing the data for the last recorded error.


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
<i>ppszErrorInfo</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  The error information returned in  <i>ppszErrorInfo</i> must be released with <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a> when it is no longer required for use.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 

