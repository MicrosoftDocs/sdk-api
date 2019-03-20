---
UID: NF:wsdclient.IWSDDeviceProxy.EndGetMetadata
title: IWSDDeviceProxy::EndGetMetadata (wsdclient.h)
author: windows-sdk-content
description: Ends an asynchronous request for metadata.
old-location: ncd\iwsddeviceproxy_endgetmetadata.htm
tech.root: WsdApi
ms.assetid: c59ee37f-9189-4c32-8404-23cc94d76ad9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndGetMetadata, EndGetMetadata method, EndGetMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,EndGetMetadata method, IWSDDeviceProxy.EndGetMetadata, IWSDDeviceProxy::EndGetMetadata, ncd.iwsddeviceproxy_endgetmetadata, wsdclient/IWSDDeviceProxy::EndGetMetadata
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
 - IWSDDeviceProxy.EndGetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceProxy::EndGetMetadata


## -description


Ends an asynchronous request for metadata and returns the metadata related to a device.


## -parameters




### -param pResult [in]

The <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object returned by <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pResult</i> is <b>NULL</b>.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. The metadata was not returned, was invalid, or a fault was generated.

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



EndGetMetadata must only be called after the <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> object returned by <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> has indicated that the operation is complete.  Once EndGetMetadata has been called, the results of the latest metadata retrieval are accessible through the <a href="https://msdn.microsoft.com/3a0a3954-348f-4a9d-9e52-f72d29ec0425">GetAllMetadata</a>, <a href="https://msdn.microsoft.com/e1e81f75-baeb-4406-8de0-f575db573fe8">GetHostMetadata</a>, <a href="https://msdn.microsoft.com/95a87bb1-8e62-4ece-a7bc-2483ea282ede">GetThisDeviceMetadata</a>, and <a href="https://msdn.microsoft.com/8a9343b8-34f3-41f9-8b02-853ae724ec75">GetThisModelMetadata</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

