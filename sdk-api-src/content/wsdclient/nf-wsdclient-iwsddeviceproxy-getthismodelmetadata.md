---
UID: NF:wsdclient.IWSDDeviceProxy.GetThisModelMetadata
title: IWSDDeviceProxy::GetThisModelMetadata
author: windows-sdk-content
description: Retrieves model-specific metadata for the device.
old-location: ncd\iwsddeviceproxy_getthismodelmetadata_method.htm
tech.root: wsdapi
ms.assetid: 8a9343b8-34f3-41f9-8b02-853ae724ec75
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetThisModelMetadata, GetThisModelMetadata method, GetThisModelMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetThisModelMetadata method, IWSDDeviceProxy.GetThisModelMetadata, IWSDDeviceProxy::GetThisModelMetadata, ncd.iwsddeviceproxy_getthismodelmetadata_method, wsdclient/IWSDDeviceProxy::GetThisModelMetadata
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
 - IWSDDeviceProxy.GetThisModelMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceProxy::GetThisModelMetadata


## -description


Retrieves model-specific metadata for the device.


## -parameters




### -param ppManufacturerMetadata [out]

Reference to a <a href="https://msdn.microsoft.com/614daaeb-76ac-4dec-93fe-f413164d5330">WSD_THIS_MODEL_METADATA</a> structure that specifies manufacturer and model-specific metadata. Do not release this object.


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
<i>ppManufacturerMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>GetThisModelMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetThisModelMetadata</b> will return the metadata retrieved with the last call to <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> and <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetThisModelMetadata</b> will return the metadata retrieved when the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a>  or <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a> is called or until the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object is released.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

