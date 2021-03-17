---
UID: NF:wsdhost.IWSDDeviceHost.SetMetadata
title: IWSDDeviceHost::SetMetadata (wsdhost.h)
description: Sets the metadata for a device, excluding user-defined service metadata.
helpviewer_keywords: ["IWSDDeviceHost interface","SetMetadata method","IWSDDeviceHost.SetMetadata","IWSDDeviceHost::SetMetadata","SetMetadata","SetMetadata method","SetMetadata method","IWSDDeviceHost interface","ncd.iwsddevicehost_setmetadata_method","wsdhost/IWSDDeviceHost::SetMetadata"]
old-location: ncd\iwsddevicehost_setmetadata_method.htm
tech.root: ncd
ms.assetid: dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,SetMetadata method, IWSDDeviceHost.SetMetadata, IWSDDeviceHost::SetMetadata, SetMetadata, SetMetadata method, SetMetadata method,IWSDDeviceHost interface, ncd.iwsddevicehost_setmetadata_method, wsdhost/IWSDDeviceHost::SetMetadata
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceHost::SetMetadata
 - wsdhost/IWSDDeviceHost::SetMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.SetMetadata
---

# IWSDDeviceHost::SetMetadata


## -description

Sets the metadata for a device, excluding user-defined service metadata.

## -parameters

### -param pThisModelMetadata [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_model_metadata">WSD_THIS_MODEL_METADATA</a> structure which specifies metadata that is common to all instances of the model of this device. 
The <b>Manufacturer</b>, <b>ModelNames</b>, and <b>ModelNumber</b> members of the structure must contain non-<b>NULL</b>, non-blank entries.

### -param pThisDeviceMetadata [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_this_device_metadata">WSD_THIS_DEVICE_METADATA</a> structure which specifies metadata unique to this device. The <b>FriendlyName</b>, <b>FirmwareVersion</b>, and <b>SerialNumber</b> members of this structure must contain non-<b>NULL</b>, non-blank entries.

### -param pHostMetadata [in, optional]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_host_metadata">WSD_HOST_METADATA</a> structure that specifies service host metadata, which the specific data and characteristics of the device (for example, a printer supports color or has a stapler.).

### -param pCustomMetadata [in, optional]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_metadata_section_list">WSD_METADATA_SECTION_LIST</a> structure which specifies additional custom metadata associated with this device.

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
<i>pThisDeviceMetadata</i> is <b>NULL</b>,  <i>pThisModelMetadata</i> is <b>NULL</b>, or either structure does not contain the required members. See the parameter descriptions for a list of required members.

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

This method must be called at least once prior to starting any device host which was registered with <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-registerservice">RegisterService</a>. It may be called after the device is started to update the metadata, in which case WS-Discovery Hello messages are issued indicating the new metadata version. 

<div class="alert"><b>Note</b>  The update feature has not yet been implemented.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>