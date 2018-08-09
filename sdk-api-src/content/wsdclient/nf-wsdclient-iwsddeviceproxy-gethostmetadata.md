---
UID: NF:wsdclient.IWSDDeviceProxy.GetHostMetadata
title: IWSDDeviceProxy::GetHostMetadata
author: windows-sdk-content
description: Retrieves class-specific metadata for the device describing the features of the device and the services it hosts.
old-location: ncd\iwsddeviceproxy_gethostmetadata.htm
old-project: wsdapi
ms.assetid: e1e81f75-baeb-4406-8de0-f575db573fe8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetHostMetadata, GetHostMetadata method, GetHostMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetHostMetadata method, IWSDDeviceProxy.GetHostMetadata, IWSDDeviceProxy::GetHostMetadata, ncd.iwsddeviceproxy_gethostmetadata, wsdclient/IWSDDeviceProxy::GetHostMetadata
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
 - IWSDDeviceProxy.GetHostMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceProxy::GetHostMetadata


## -description


Retrieves class-specific metadata for the device describing the features of the device and the services it hosts.


## -parameters




### -param ppHostMetadata [out]

Reference to a <a href="https://msdn.microsoft.com/da774582-3b27-470d-9b6a-ac2b106a47b9">WSD_HOST_METADATA</a> structure that specifies metadata. 
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
<i>ppHostMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>GetHostMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetHostMetadata</b> will return the metadata retrieved with the last call to <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> and <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetHostMetadata</b> will return the metadata retrieved when the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> or <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a> is called or until the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object is released.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

