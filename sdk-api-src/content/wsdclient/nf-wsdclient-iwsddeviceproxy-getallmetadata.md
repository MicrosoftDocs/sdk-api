---
UID: NF:wsdclient.IWSDDeviceProxy.GetAllMetadata
title: IWSDDeviceProxy::GetAllMetadata
author: windows-driver-content
description: Retrieves all metadata for this device.
old-location: ncd\iwsddeviceproxy_getallmetadata_method.htm
old-project: WsdApi
ms.assetid: 3a0a3954-348f-4a9d-9e52-f72d29ec0425
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetAllMetadata, GetAllMetadata method, GetAllMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetAllMetadata method, IWSDDeviceProxy.GetAllMetadata, IWSDDeviceProxy::GetAllMetadata, ncd.iwsddeviceproxy_getallmetadata_method, wsdclient/IWSDDeviceProxy::GetAllMetadata
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDDeviceProxy.GetAllMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDDeviceProxy::GetAllMetadata


## -description


Retrieves all metadata for this device.


## -parameters




### -param ppMetadata [out]

Reference to a <a href="https://msdn.microsoft.com/e5c6373a-f365-499d-a971-472ffa557a41">WSD_METADATA_SECTION_LIST</a> structure that specifies all metadata related to a device. 
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
<i>ppMetadata</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is supplied so that extended metadata may be accessed. Manufacturer, service host and device-specific metadata is best obtained using methods provided specifically for those purposes.



<b>GetAllMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetAllMetadata</b> will return the metadata retrieved with the last call to <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> and <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetAllMetadata</b> will return the metadata retrieved when the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">BeginGetMetadata</a> or <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">EndGetMetadata</a> is called, or until the <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object is released.




## -see-also




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

