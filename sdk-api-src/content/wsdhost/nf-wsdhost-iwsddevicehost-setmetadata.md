---
UID: NF:wsdhost.IWSDDeviceHost.SetMetadata
title: IWSDDeviceHost::SetMetadata
author: windows-sdk-content
description: Sets the metadata for a device, excluding user-defined service metadata.
old-location: ncd\iwsddevicehost_setmetadata_method.htm
tech.root: wsdapi
ms.assetid: dc4cbed9-9ec4-4bbd-b1c9-89c4c11ff424
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWSDDeviceHost interface,SetMetadata method, IWSDDeviceHost.SetMetadata, IWSDDeviceHost::SetMetadata, SetMetadata, SetMetadata method, SetMetadata method,IWSDDeviceHost interface, ncd.iwsddevicehost_setmetadata_method, wsdhost/IWSDDeviceHost::SetMetadata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.SetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDDeviceHost::SetMetadata


## -description


Sets the metadata for a device, excluding user-defined service metadata.


## -parameters




### -param pThisModelMetadata [in]

Reference to a <a href="https://msdn.microsoft.com/614daaeb-76ac-4dec-93fe-f413164d5330">WSD_THIS_MODEL_METADATA</a> structure which specifies metadata that is common to all instances of the model of this device. 
The <b>Manufacturer</b>, <b>ModelNames</b>, and <b>ModelNumber</b> members of the structure must contain non-<b>NULL</b>, non-blank entries.


### -param pThisDeviceMetadata [in]

Reference to a <a href="https://msdn.microsoft.com/7b9d063f-f0d5-4333-a5d8-e9a6d2d9af88">WSD_THIS_DEVICE_METADATA</a> structure which specifies metadata unique to this device. The <b>FriendlyName</b>, <b>FirmwareVersion</b>, and <b>SerialNumber</b> members of this structure must contain non-<b>NULL</b>, non-blank entries.


### -param pHostMetadata [in, optional]

Reference to a <a href="https://msdn.microsoft.com/da774582-3b27-470d-9b6a-ac2b106a47b9">WSD_HOST_METADATA</a> structure that specifies service host metadata, which the specific data and characteristics of the device (for example, a printer supports color or has a stapler.).


### -param pCustomMetadata [in, optional]

Reference to a <a href="https://msdn.microsoft.com/e5c6373a-f365-499d-a971-472ffa557a41">WSD_METADATA_SECTION_LIST</a> structure which specifies additional custom metadata associated with this device. 


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



This method must be called at least once prior to starting any device host which was registered with <a href="https://msdn.microsoft.com/8e125e72-4060-4be6-b370-b2f6b24d9da7">RegisterService</a>. It may be called after the device is started to update the metadata, in which case WS-Discovery Hello messages are issued indicating the new metadata version. 

<div class="alert"><b>Note</b>  The update feature has not yet been implemented.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a>
 

 

