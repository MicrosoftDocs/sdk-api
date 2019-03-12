---
UID: NF:wsdclient.IWSDDeviceProxy.BeginGetMetadata
title: IWSDDeviceProxy::BeginGetMetadata
author: windows-sdk-content
description: Sends an asynchronous request for metadata.
old-location: ncd\iwsddeviceproxy_begingetmetadata.htm
tech.root: WsdApi
ms.assetid: 8aa71ef1-61b9-411b-9e8c-75470c638469
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginGetMetadata, BeginGetMetadata method, BeginGetMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,BeginGetMetadata method, IWSDDeviceProxy.BeginGetMetadata, IWSDDeviceProxy::BeginGetMetadata, ncd.iwsddeviceproxy_begingetmetadata, wsdclient/IWSDDeviceProxy::BeginGetMetadata
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
 - IWSDDeviceProxy.BeginGetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceProxy::BeginGetMetadata


## -description


Sends an asynchronous request for metadata.


## -parameters




### -param ppResult [out]

Returns an <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object that can be used to determine whether an operation has completed.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppResult</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The method could not be completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



BeginGetMetadata will force the device proxy to send a metadata request to the host.  Once <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a> has been called, the results of the latest metadata retrieval are accessible through the <a href="https://msdn.microsoft.com/3a0a3954-348f-4a9d-9e52-f72d29ec0425">GetAllMetadata</a>, <a href="https://msdn.microsoft.com/e1e81f75-baeb-4406-8de0-f575db573fe8">GetHostMetadata</a>, <a href="https://msdn.microsoft.com/95a87bb1-8e62-4ece-a7bc-2483ea282ede">GetThisDeviceMetadata</a>, and <a href="https://msdn.microsoft.com/8a9343b8-34f3-41f9-8b02-853ae724ec75">GetThisModelMetadata</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

