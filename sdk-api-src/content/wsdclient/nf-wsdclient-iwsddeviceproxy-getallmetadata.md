---
UID: NF:wsdclient.IWSDDeviceProxy.GetAllMetadata
title: IWSDDeviceProxy::GetAllMetadata (wsdclient.h)
author: windows-sdk-content
description: Retrieves all metadata for this device.
old-location: ncd\iwsddeviceproxy_getallmetadata_method.htm
tech.root: WsdApi
ms.assetid: 3a0a3954-348f-4a9d-9e52-f72d29ec0425
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllMetadata, GetAllMetadata method, GetAllMetadata method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetAllMetadata method, IWSDDeviceProxy.GetAllMetadata, IWSDDeviceProxy::GetAllMetadata, ncd.iwsddeviceproxy_getallmetadata_method, wsdclient/IWSDDeviceProxy::GetAllMetadata
ms.topic: method
f1_keywords:
- wsdclient/IWSDDeviceProxy.GetAllMetadata
dev_langs:
 - c++
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
- IWSDDeviceProxy.GetAllMetadata
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDDeviceProxy::GetAllMetadata


## -description


Retrieves all metadata for this device.


## -parameters




### -param ppMetadata [out]

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_metadata_section_list">WSD_METADATA_SECTION_LIST</a> structure that specifies all metadata related to a device. 
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



<b>GetAllMetadata</b> will not cause the device proxy to retrieve metadata from the device.  Instead, <b>GetAllMetadata</b> will return the metadata retrieved with the last call to <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a>.  If neither of these methods has been called, <b>GetAllMetadata</b> will return the metadata retrieved when the <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object was initialized.

Upon success, the memory at <i>ppMetadata</i> will be valid until <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">BeginGetMetadata</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">EndGetMetadata</a> is called, or until the <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object is released.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>
 

 

