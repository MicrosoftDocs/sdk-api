---
UID: NF:mftransform.IMFDeviceTransform.ProcessOutput
title: IMFDeviceTransform::ProcessOutput
author: windows-sdk-content
description: The ProcessOutput method gets the processed output from the Device MFT output streams.
old-location: stream\imfdevicetransform_processoutput.htm
old-project: stream
ms.assetid: A99242D6-5225-493C-A5A8-CFDBB49D01A0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMFDeviceTransform interface [Streaming Media Devices],ProcessOutput method, IMFDeviceTransform.ProcessOutput, IMFDeviceTransform::ProcessOutput, ProcessOutput, ProcessOutput method [Streaming Media Devices], ProcessOutput method [Streaming Media Devices],IMFDeviceTransform interface, mftransform/IMFDeviceTransform::ProcessOutput, stream.imfdevicetransform_processoutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.ProcessOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDeviceTransform::ProcessOutput


## -description


The <b>ProcessOutput</b> method gets the processed output from the Device MFT output streams.


## -parameters




### -param dwFlags [in]

Bitwise OR of zero or more flags from the <a href="https://msdn.microsoft.com/846e91a5-7cd8-4b58-9484-b9cb9af0bebf">_MFT_PROCESS_OUTPUT_FLAGS</a> enumeration.


### -param cOutputBufferCount [in]

Number of elements in the <i>pOutputSamples</i> array. The value must be at least 1.


### -param pOutputSample




### -param pdwStatus [in]

Receives a bitwise OR of zero or more flags from the <a href="https://msdn.microsoft.com/80804b33-1dac-41f8-8446-8f929bf9b931">_MFT_PROCESS_OUTPUT_STATUS</a> enumeration.


#### - pOutputSamples [in]

Pointer to an array of <a href="https://msdn.microsoft.com/57623c8f-f7b6-4cb3-8d54-4ee516c706c3">MFT_OUTPUT_DATA_BUFFER</a> structures, allocated by the caller. The MFT uses this array to return output data to the caller.


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



In most cases, if the method succeeds, the Media Foundation transform (MFT) stores the sample and holds a reference count on the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> pointer. When the MFT is done using the sample, it must release it to avoid memory leaks.


After the device transform manager (DTM) has set valid media types on all of the streams, the MFT should always be able to accept more input and be able to produce more output. 


If an MFT encounters a non-fatal error in the input data, it can simply drop the data and attempt to recover when it gets the more input data. If the MFT drops any data, it should set the <a href="https://msdn.microsoft.com/f9e1e700-9958-404d-8b83-08f846f5a1b0">MFSampleExtension_Discontinuity</a> attribute on the next output sample, to notify the caller that there is a gap in the data stream.





## -see-also




<a href="https://msdn.microsoft.com/375293FA-8017-4F74-A93C-C15FED8F19AF">IMFDeviceTransform</a>
 

 

