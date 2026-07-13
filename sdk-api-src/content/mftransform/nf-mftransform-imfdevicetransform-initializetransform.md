---
UID: NF:mftransform.IMFDeviceTransform.InitializeTransform
title: IMFDeviceTransform::InitializeTransform (mftransform.h)
description: InitializeTransform is called to initialize the Device MFT.
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","InitializeTransform method","IMFDeviceTransform.InitializeTransform","IMFDeviceTransform::InitializeTransform","InitializeTransform","InitializeTransform method [Streaming Media Devices]","InitializeTransform method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::InitializeTransform","stream.imfdevicetransform_initializetransform"]
old-location: stream\imfdevicetransform_initializetransform.htm
tech.root: stream
ms.assetid: 02ACBC34-0514-4EAE-AC48-62F6AE219E93
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],InitializeTransform method, IMFDeviceTransform.InitializeTransform, IMFDeviceTransform::InitializeTransform, InitializeTransform, InitializeTransform method [Streaming Media Devices], InitializeTransform method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::InitializeTransform, stream.imfdevicetransform_initializetransform
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDeviceTransform::InitializeTransform
 - mftransform/IMFDeviceTransform::InitializeTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.InitializeTransform
---

# IMFDeviceTransform::InitializeTransform


## -description

<b>InitializeTransform</b> is called to initialize the Device MFT.

## -parameters

### -param pAttributes [in]

Contains a pointer to an attribute, passed in by the capture pipeline that contains initialization parameters. The following attributes values are passed to the function
<table>
<tr>
<th>Attribute Key</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_DEVICEMFT_CONNECTED_FILTER_KSCONTROL</b></dt>
</dl>
</td>
<td width="60%">
The IKsControl interface of the preceding DeviceTransform object. It also implements IMFDeviceTransform, used to get necessary information needed to create a valid pipeline.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</b></dt>
</dl>
</td>
<td width="60%">
Denotes the symbolic link for a video capture driver

</td>
</tr>
 <tr>
<td width="40%">
<dl>
<dt><b>MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME</b></dt>
</dl>
</td>
<td width="60%">
Specifies the display name for a device. The display name is a human-readable string, suitable for display in a user interface.
</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include but not limited to values given in the following table.

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
Initialization succeeded

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Device MFT could not  support the request at this time.

</td>
</tr>
</table>

## -remarks

Device MFTs can take advantage of this function to initialize various internal objects and states. Pipeline can also use the input <i>IMFAttributes</i> parameter to communicate certain configuration information to the Device MFT.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>
