---
UID: NF:wmcontainer.IMFASFSplitter.ParseData
title: IMFASFSplitter::ParseData (wmcontainer.h)
author: windows-sdk-content
description: Sends packetized Advanced Systems Format (ASF) data to the ASF splitter for processing.
old-location: mf\imfasfsplitter_parsedata.htm
tech.root: medfound
ms.assetid: 13457c17-ab35-47a3-8e83-00eef7686841
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 13457c17-ab35-47a3-8e83-00eef7686841, IMFASFSplitter interface [Media Foundation],ParseData method, IMFASFSplitter.ParseData, IMFASFSplitter::ParseData, ParseData, ParseData method [Media Foundation], ParseData method [Media Foundation],IMFASFSplitter interface, mf.imfasfsplitter_parsedata, wmcontainer/IMFASFSplitter::ParseData
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
 - IMFASFSplitter.ParseData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFSplitter::ParseData


## -description



Sends packetized Advanced Systems Format (ASF) data to the ASF splitter for processing.




## -parameters




### -param pIBuffer [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of a buffer object containing data to be parsed.


### -param cbBufferOffset [in]

The offset into the data buffer where the splitter should begin parsing. This value is typically set to 0.


### -param cbLength [in]

The length, in bytes, of the data to parse. This value is measured from the offset specified by <i>cbBufferOffset</i>. Set to 0 to process to the end of the buffer.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIBuffer</i> parameter is <b>NULL</b>.

The specified offset value in <i>cbBufferOffset</i> is greater than the length of the buffer.

The total value of <i>cbBufferOffset</i> and <i>cbLength</i> is greater than the length of the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize">IMFASFSplitter::Initialize</a> method was not called or the call failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The splitter cannot process more input at this time.

</td>
</tr>
</table>
 




## -remarks



After using this method to parse data, you must call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample">IMFASFSplitter::GetNextSample</a> to retrieve parsed media samples.

If your ASF data contains variable-sized packets, you must set the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfasfsplitter-packet-boundary-attribute">MFASFSPLITTER_PACKET_BOUNDARY</a> attribute on the buffers to indicate the sample boundaries, and the buffers cannot span multiple packets.

If the method returns ME_E_NOTACCEPTING, call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample">GetNextSample</a> to get the output samples, or call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush">IMFASFSplitter::Flush</a> to clear the splitter.

The splitter might hold a reference count on the input buffer. Therefore, do not write over the valid data in the buffer after calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-splitter">ASF Splitter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter">IMFASFSplitter</a>
 

 

