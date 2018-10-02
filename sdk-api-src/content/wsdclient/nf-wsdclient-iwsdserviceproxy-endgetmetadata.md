---
UID: NF:wsdclient.IWSDServiceProxy.EndGetMetadata
title: IWSDServiceProxy::EndGetMetadata
author: windows-sdk-content
description: Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.
old-location: ncd\iwsdserviceproxy_endgetmetadata.htm
tech.root: WsdApi
ms.assetid: 6024770a-e4cb-4db1-9767-51b559fd8244
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EndGetMetadata, EndGetMetadata method, EndGetMetadata method,IWSDServiceProxy interface, IWSDServiceProxy interface,EndGetMetadata method, IWSDServiceProxy.EndGetMetadata, IWSDServiceProxy::EndGetMetadata, ncd.iwsdserviceproxy_endgetmetadata, wsdclient/IWSDServiceProxy::EndGetMetadata
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
 - IWSDServiceProxy.EndGetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxy::EndGetMetadata


## -description


Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.


## -parameters




### -param pResult [in]

An <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that represents the result of the request. Release this object when done.


### -param ppMetadata [out]

Requested metadata. For details, see <a href="https://msdn.microsoft.com/e5c6373a-f365-499d-a971-472ffa557a41">WSD_METADATA_SECTION_LIST</a>. Do not release this object.


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
</table>
 




## -remarks



<b>EndGetMetadata</b> may block until the metadata retrieval operation has completed.




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

