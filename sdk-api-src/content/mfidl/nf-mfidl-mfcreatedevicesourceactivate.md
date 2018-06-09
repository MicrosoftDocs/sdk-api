---
UID: NF:mfidl.MFCreateDeviceSourceActivate
title: MFCreateDeviceSourceActivate function
author: windows-sdk-content
description: Creates an activation object that represents a hardware capture device.
old-location: mf\mfcreatedevicesourceactivate.htm
old-project: medfound
ms.assetid: c52cb35a-8f5b-479e-9c08-3185c9a561f2
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateDeviceSourceActivate, MFCreateDeviceSourceActivate function [Media Foundation], mf.mfcreatedevicesourceactivate, mfidl/MFCreateDeviceSourceActivate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateDeviceSourceActivate
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateDeviceSourceActivate function


## -description


Creates an activation object that represents a hardware capture device.


## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store, which is used to select the device. See Remarks.


### -param ppActivate [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. The caller must release the interface.


## -remarks



This function creates an activation object that can be used to create a media source for a hardware device. To create the media source itself, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a>.

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




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/8a9d96f8-1096-4b66-a2ec-8a95d754ea72">Audio/Video Capture in Media Foundation</a>



<a href="https://msdn.microsoft.com/dd24671a-0689-4490-8d18-2a33ed461e9d">Capture Device Attributes</a>



<a href="https://msdn.microsoft.com/9f80b604-1cc2-4d0d-b94e-a2b9dab1fdde">MFCreateDeviceSource</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

