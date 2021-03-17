---
UID: NF:mftransform.IMFDeviceTransform.ProcessOutput
title: IMFDeviceTransform::ProcessOutput (mftransform.h)
description: The ProcessOutput method gets the processed output from the Device MFT output streams.
helpviewer_keywords: ["IMFDeviceTransform interface [Streaming Media Devices]","ProcessOutput method","IMFDeviceTransform.ProcessOutput","IMFDeviceTransform::ProcessOutput","ProcessOutput","ProcessOutput method [Streaming Media Devices]","ProcessOutput method [Streaming Media Devices]","IMFDeviceTransform interface","mftransform/IMFDeviceTransform::ProcessOutput","stream.imfdevicetransform_processoutput"]
old-location: stream\imfdevicetransform_processoutput.htm
tech.root: stream
ms.assetid: A99242D6-5225-493C-A5A8-CFDBB49D01A0
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],ProcessOutput method, IMFDeviceTransform.ProcessOutput, IMFDeviceTransform::ProcessOutput, ProcessOutput, ProcessOutput method [Streaming Media Devices], ProcessOutput method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::ProcessOutput, stream.imfdevicetransform_processoutput
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
 - IMFDeviceTransform::ProcessOutput
 - mftransform/IMFDeviceTransform::ProcessOutput
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
 - IMFDeviceTransform.ProcessOutput
---

# IMFDeviceTransform::ProcessOutput


## -description

The <b>ProcessOutput</b> method gets the processed output from the Device MFT output streams.

## -parameters

### -param dwFlags [in]

Bitwise OR of zero or more flags from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_flags">_MFT_PROCESS_OUTPUT_FLAGS</a> enumeration.

### -param cOutputBufferCount [in]

Number of elements in the <i>pOutputSamples</i> array. The value must be at least 1.

### -param pOutputSample [in]

Pointer to an array of <a href="/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer">MFT_OUTPUT_DATA_BUFFER</a> structures, allocated by the caller. The MFT uses this array to return output data to the caller.

### -param pdwStatus [in]

Receives a bitwise OR of zero or more flags from the <a href="/windows/win32/api/mftransform/ne-mftransform-_mft_process_output_status">_MFT_PROCESS_OUTPUT_STATUS</a> enumeration.

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

In most cases, if the method succeeds, the Media Foundation transform (MFT) stores the sample and holds a reference count on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> pointer. When the MFT is done using the sample, it must release it to avoid memory leaks.


After the device transform manager (DTM) has set valid media types on all of the streams, the MFT should always be able to accept more input and be able to produce more output. 


If an MFT encounters a non-fatal error in the input data, it can simply drop the data and attempt to recover when it gets the more input data. If the MFT drops any data, it should set the <a href="/windows/desktop/medfound/mfsampleextension-discontinuity-attribute">MFSampleExtension_Discontinuity</a> attribute on the next output sample, to notify the caller that there is a gap in the data stream.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>