---
UID: NF:wsdclient.IWSDDeviceProxy.GetThisDeviceMetadata
title: IWSDDeviceProxy::GetThisDeviceMetadata
author: windows-sdk-content
description: Retrieves device-specific metadata for this device.
old-location: ncd\iwsddeviceproxy_getthisdevicemetadata_method.htm
old-project: WsdApi
ms.assetid: 95a87bb1-8e62-4ece-a7bc-2483ea282ede
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetThisDeviceMetadata, GetThisDeviceMetadata method, GetThisDeviceMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetThisDeviceMetadata method, IWSDDeviceProxy.GetThisDeviceMetadata, IWSDDeviceProxy::GetThisDeviceMetadata, ncd.iwsddeviceproxy_getthisdevicemetadata_method, wsdclient/IWSDDeviceProxy::GetThisDeviceMetadata
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceProxy.GetThisDeviceMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceProxy::GetThisDeviceMetadata


## -description


Retrieves device-specific metadata for this device.


## -parameters




### -param ppThisDeviceMetadata [out]

Reference to a <a href="https://msdn.microsoft.com/7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88">WSD_THIS_DEVICE_METADATA</a> structure that specifies the device-specific metadata of this device. 
Do not release this object.


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
<i>ppThisDeviceMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>GetThisDeviceMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetThisDeviceMetadata</b> will return the metadata retrieved with the last call to <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> and <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetThisDeviceMetadata</b> will return the metadata retrieved when the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> or <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a> is called or until the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object is released.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

