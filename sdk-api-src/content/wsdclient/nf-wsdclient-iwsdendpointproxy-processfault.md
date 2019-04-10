---
UID: NF:wsdclient.IWSDEndpointProxy.ProcessFault
title: IWSDEndpointProxy::ProcessFault (wsdclient.h)
author: windows-sdk-content
description: Processes a SOAP fault retrieved by GetFaultInfo.
old-location: ncd\iwsdendpointproxy_processfault.htm
tech.root: WsdApi
ms.assetid: f63c8c7c-8581-49d4-a29d-a7b0b46a2db5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDEndpointProxy interface,ProcessFault method, IWSDEndpointProxy.ProcessFault, IWSDEndpointProxy::ProcessFault, ProcessFault, ProcessFault method, ProcessFault method,IWSDEndpointProxy interface, ncd.iwsdendpointproxy_processfault, wsdclient/IWSDEndpointProxy::ProcessFault
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
 - IWSDEndpointProxy.ProcessFault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy::ProcessFault


## -description


Processes a SOAP fault retrieved by <a href="https://msdn.microsoft.com/45ed30fd-7e4f-44f5-bb90-5686746e39be">GetFaultInfo</a>.


## -parameters




### -param pFault [in]

Pointer to a <a href="https://msdn.microsoft.com/ed5e2575-203a-41a2-b656-50cb82aae088">WSD_SOAP_FAULT</a> structure containing the fault data.


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
<i>pFault</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The fault was not stored in memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a>
 

 

