---
UID: NF:mftransform.IMFDeviceTransform.ProcessMessage
title: IMFDeviceTransform::ProcessMessage (mftransform.h)
description: The ProcessMessage method sends a message to the Device Media Foundation transform (MFT).
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","ProcessMessage method","IMFDeviceTransform.ProcessMessage","IMFDeviceTransform::ProcessMessage","ProcessMessage","ProcessMessage method [Streaming Media Devices]","ProcessMessage method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::ProcessMessage","stream.imfdevicetransform_processmessage"]
old-location: stream\imfdevicetransform_processmessage.htm
tech.root: stream
ms.assetid: 890CAC55-CF9E-420C-ACFC-5A92E53258AA
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],ProcessMessage method, IMFDeviceTransform.ProcessMessage, IMFDeviceTransform::ProcessMessage, ProcessMessage, ProcessMessage method [Streaming Media Devices], ProcessMessage method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::ProcessMessage, stream.imfdevicetransform_processmessage
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
 - IMFDeviceTransform::ProcessMessage
 - mftransform/IMFDeviceTransform::ProcessMessage
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
 - IMFDeviceTransform.ProcessMessage
---

# IMFDeviceTransform::ProcessMessage


## -description

The    <b>ProcessMessage</b> method sends a message to the Device Media Foundation transform (MFT).

## -parameters

### -param eMessage [in]

The message to send, specified as a member of the <a href="/windows/desktop/api/mftransform/ne-mftransform-mft_message_type">MFT_MESSAGE_TYPE</a> enumeration.

### -param ulParam [in]

Message parameter. The meaning of this parameter depends on the message type.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument passed.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVAILIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
An invalid stream ID was passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_STREAM_STATE</b></dt>
</dl>
</td>
<td width="60%">
The requested stream transition is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
Input media type has not been set.

</td>
</tr>
</table>

## -remarks

Before calling this method, set the media types on all input and output streams.

The MFT might ignore certain message types. If so, the method returns <b>S_OK</b>. An error code indicates that the transform handles this message type but was unable to process the message in this instance.

For more information, see <a href="/windows/desktop/api/mftransform/ne-mftransform-mft_message_type">MFT_MESSAGE_TYPE</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>