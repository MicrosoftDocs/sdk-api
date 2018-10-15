---
UID: NF:wmcontainer.IMFASFMultiplexer.ProcessSample
title: IMFASFMultiplexer::ProcessSample
author: windows-sdk-content
description: Delivers input samples to the multiplexer.
old-location: mf\imfasfmultiplexer_processsample.htm
tech.root: medfound
ms.assetid: 30a693bb-255c-47a4-8102-1543872b0a5e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 30a693bb-255c-47a4-8102-1543872b0a5e, IMFASFMultiplexer interface [Media Foundation],ProcessSample method, IMFASFMultiplexer.ProcessSample, IMFASFMultiplexer::ProcessSample, ProcessSample, ProcessSample method [Media Foundation], ProcessSample method [Media Foundation],IMFASFMultiplexer interface, mf.imfasfmultiplexer_processsample, wmcontainer/IMFASFMultiplexer::ProcessSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer.ProcessSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMultiplexer::ProcessSample


## -description


Delivers input samples to the multiplexer.
        


## -parameters




### -param wStreamNumber [in]

The stream number of the stream to which the sample belongs.
          


### -param pISample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the input sample. The input sample contains the media data to be converted to ASF data packets. When possible, the time stamp of this sample should be accurate.
          


### -param hnsTimestampAdjust [in]

The adjustment to apply to the time stamp of the sample. This parameter is used if the caller wants to shift the sample time on <i>pISample</i>. This value should be positive if the time stamp should be pushed ahead and negative if the time stamp should be pushed back. This time stamp is added to sample time on <i>pISample</i>, and the resulting time is used by the multiplexer instead of the original sample time. If no adjustment is needed, set this value to 0.
          


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
There are too many packets waiting to be retrieved from the multiplexer. Call <a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">IMFASFMultiplexer::GetNextPacket</a> to get the packets.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BANDWIDTH_OVERRUN</b></dt>
</dl>
</td>
<td width="60%">
The sample that was processed violates the bandwidth limitations specified for the stream in the ASF ContentInfo object. When this error is generated, the sample is dropped.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The value passed in <i>wStreamNumber</i> is invalid.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_LATE_SAMPLE</b></dt>
</dl>
</td>
<td width="60%">
The presentation time of the input media sample is earlier than the send time.
              

</td>
</tr>
</table>
 




## -remarks



The application passes samples to <b>ProcessSample</b>, and the ASF multiplexer queues them internally until they are ready to be placed into ASF packets. Call <a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">IMFASFMultiplexer::GetNextPacket</a> to get the ASF data packet.
      

After each call to <b>ProcessSample</b>, call <a href="https://msdn.microsoft.com/39b9f8a0-fb26-4f46-98fd-b4636f8f88c7">GetNextPacket</a> in a loop to get all of the available data packets. For a code example, see <a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>.




## -see-also




<a href="https://msdn.microsoft.com/7afa9694-c965-40e2-8549-e32ff48def2a">Generating New ASF Data Packets</a>



<a href="https://msdn.microsoft.com/bdb549b5-425b-4f77-b413-723ceb7acd11">IMFASFMultiplexer</a>



<a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>
 

 

