---
UID: NF:wsdclient.IWSDServiceProxy.GetServiceMetadata
title: IWSDServiceProxy::GetServiceMetadata
author: windows-sdk-content
description: Retrieves the metadata for the IWSDServiceProxy object.
old-location: ncd\iwsdserviceproxy_getservicemetadata_method.htm
old-project: WsdApi
ms.assetid: 552da68f-6e6a-44b2-8c95-e29bc67de3c2
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetServiceMetadata, GetServiceMetadata method, GetServiceMetadata method,IWSDServiceProxy interface, IWSDServiceProxy interface,GetServiceMetadata method, IWSDServiceProxy.GetServiceMetadata, IWSDServiceProxy::GetServiceMetadata, ncd.iwsdserviceproxy_getservicemetadata_method, wsdclient/IWSDServiceProxy::GetServiceMetadata
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDServiceProxy.GetServiceMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxy::GetServiceMetadata


## -description


Retrieves the metadata for the <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> object.


## -parameters




### -param ppServiceMetadata [out]

Reference to a <a href="https://msdn.microsoft.com/1f80e36f-06ca-41fc-bbd7-b44823c75d4d">WSD_SERVICE_METADATA</a> structure that specifies service metadata. Do not release this object.


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
<i>ppServiceMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This metadata is also available as part of the metadata produced by <a href="https://msdn.microsoft.com/e1e81f75-baeb-4406-8de0-f575db573fe8">IWSDDeviceProxy::GetHostMetadata</a>.




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

