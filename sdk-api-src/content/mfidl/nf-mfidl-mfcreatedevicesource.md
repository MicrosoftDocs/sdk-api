---
UID: NF:mfidl.MFCreateDeviceSource
title: MFCreateDeviceSource function
author: windows-sdk-content
description: Creates a media source for a hardware capture device.
old-location: mf\mfcreatedevicesource.htm
tech.root: MedFound
ms.assetid: 9f80b604-1cc2-4d0d-b94e-a2b9dab1fdde
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFCreateDeviceSource, MFCreateDeviceSource function [Media Foundation], mf.mfcreatedevicesource, mfidl/MFCreateDeviceSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateDeviceSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateDeviceSource function


## -description


Creates a media source for a hardware capture device.


## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store, which is used to select the device. See Remarks.


### -param ppSource [out]

Receives a pointer to the media source's <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Important</b>  When the capture device is no longer needed, you must shut down the device by calling <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">Shutdown</a> on the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> object you obtained by calling <b>MFCreateDeviceSource</b>. Failure to call <b>Shutdown</b> can result in memory links because the system may keep a reference to <b>IMFMediaSource</b> resources until <b>Shutdown</b> is called.

</div>
<div> </div>
The <i>pAttributes</i> parameter specifies an attribute store. To create the attribute store, call the <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a> function.  You must set the <a href="https://msdn.microsoft.com/c6c05267-1c93-48e2-b463-b5a1514f1b7b">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a> attribute, which specifies the type of device (audio or video).

For audio capture devices, optionally set one of the following attributes:



<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID"></a><a id="mf_devsource_attribute_source_type_audcap_endpoint_id"></a><a href="https://msdn.microsoft.com/a0d8b54b-7a05-4307-a756-a34bb22f1afd">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a>


</td>
<td width="60%">
Specifies the audio endpoint ID of the audio capture device.

</td>
</tr>
<tr>
<td width="40%">
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE"></a><a id="mf_devsource_attribute_source_type_audcap_role"></a><a href="https://msdn.microsoft.com/4f2885b6-c771-4577-880d-5feea671432e">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE</a>


</td>
<td width="60%">
Specifies the device role. If this attribute is set, the function uses the default audio capture device for that device role.

Do not combine this attribute with the <a href="https://msdn.microsoft.com/a0d8b54b-7a05-4307-a756-a34bb22f1afd">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a> attribute.

</td>
</tr>
</table>
 

If neither attribute is specified, the function selects the default audio capture device for the <b>eCommunications</b> role.

For video capture devices, you must set the following attribute:



<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK"></a><a id="mf_devsource_attribute_source_type_vidcap_symbolic_link"></a><a href="https://msdn.microsoft.com/3d256dec-ec8c-4c62-883b-e2c292fd90eb">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a>


</td>
<td width="60%">
Specifies the symbolic link to the device.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a9d96f8-1096-4b66-a2ec-8a95d754ea72">Audio/Video Capture in Media Foundation</a>



<a href="https://msdn.microsoft.com/dd24671a-0689-4490-8d18-2a33ed461e9d">Capture Device Attributes</a>



<a href="https://msdn.microsoft.com/c52cb35a-8f5b-479e-9c08-3185c9a561f2">MFCreateDeviceSourceActivate</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

