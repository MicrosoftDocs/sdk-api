---
UID: NF:mfidl.MFCreateDeviceSourceActivate
title: MFCreateDeviceSourceActivate function (mfidl.h)
description: Creates an activation object that represents a hardware capture device.
helpviewer_keywords: ["MFCreateDeviceSourceActivate","MFCreateDeviceSourceActivate function [Media Foundation]","mf.mfcreatedevicesourceactivate","mfidl/MFCreateDeviceSourceActivate"]
old-location: mf\mfcreatedevicesourceactivate.htm
tech.root: mf
ms.assetid: c52cb35a-8f5b-479e-9c08-3185c9a561f2
ms.date: 12/05/2018
ms.keywords: MFCreateDeviceSourceActivate, MFCreateDeviceSourceActivate function [Media Foundation], mf.mfcreatedevicesourceactivate, mfidl/MFCreateDeviceSourceActivate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateDeviceSourceActivate
 - mfidl/MFCreateDeviceSourceActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateDeviceSourceActivate
---

# MFCreateDeviceSourceActivate function


## -description

Creates an activation object that represents a hardware capture device.

## -parameters

### -param pAttributes [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store, which is used to select the device. See Remarks.

### -param ppActivate [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. The caller must release the interface.

## -remarks

This function creates an activation object that can be used to create a media source for a hardware device. To create the media source itself, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a>.

The <i>pAttributes</i> parameter specifies an attribute store. To create the attribute store, call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a> function.  You must set the <a href="/windows/desktop/medfound/mf-devsource-attribute-source-type">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE</a> attribute, which specifies the type of device (audio or video).

For audio capture devices, optionally set one of the following attributes:



<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID"></a><a id="mf_devsource_attribute_source_type_audcap_endpoint_id"></a><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-audcap-endpoint-id">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a>


</td>
<td width="60%">
Specifies the audio endpoint ID of the audio capture device.

</td>
</tr>
<tr>
<td width="40%">
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE"></a><a id="mf_devsource_attribute_source_type_audcap_role"></a><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-audcap-role">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE</a>


</td>
<td width="60%">
Specifies the device role. If this attribute is set, the function uses the default audio capture device for that device role.

Do not combine this attribute with the <a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-audcap-endpoint-id">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID</a> attribute.

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
<a id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK"></a><a id="mf_devsource_attribute_source_type_vidcap_symbolic_link"></a><a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a>


</td>
<td width="60%">
Specifies the symbolic link to the device.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/medfound/audio-video-capture-in-media-foundation">Audio/Video Capture in Media Foundation</a>



<a href="/windows/desktop/medfound/capture-device-attributes">Capture Device Attributes</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource">MFCreateDeviceSource</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>