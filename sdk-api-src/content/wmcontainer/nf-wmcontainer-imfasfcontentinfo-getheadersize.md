---
UID: NF:wmcontainer.IMFASFContentInfo.GetHeaderSize
title: IMFASFContentInfo::GetHeaderSize
author: windows-sdk-content
description: Retrieves the size of the header section of an Advanced Systems Format (ASF) file.
old-location: mf\imfasfcontentinfo_getheadersize.htm
tech.root: medfound
ms.assetid: c13ee7e6-df59-448f-80c4-04ac7c8c98ed
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetHeaderSize, GetHeaderSize method [Media Foundation], GetHeaderSize method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GetHeaderSize method, IMFASFContentInfo.GetHeaderSize, IMFASFContentInfo::GetHeaderSize, c13ee7e6-df59-448f-80c4-04ac7c8c98ed, mf.imfasfcontentinfo_getheadersize, wmcontainer/IMFASFContentInfo::GetHeaderSize
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
 - IMFASFContentInfo.GetHeaderSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFContentInfo::GetHeaderSize


## -description


Retrieves the size of the header section of an Advanced Systems Format (ASF) file.
        


## -parameters




### -param pIStartOfContent [in]

The <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of a buffer object containing the beginning of ASF content. The size of the valid data in the buffer must be at least MFASF_MIN_HEADER_BYTES in bytes.


### -param cbHeaderSize [out]

Receives the size, in bytes, of the header section of the content. The value includes the size of the ASF Header Object plus the size of the header section of the Data Object. Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.


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
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer does not contain valid ASF data.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer does not contain enough valid data.
              

</td>
</tr>
</table>
 




## -remarks



The header of an ASF file or stream can be passed to the <a href="https://msdn.microsoft.com/149e2514-74e5-403b-925f-53a17dbbcb64">IMFASFContentInfo::ParseHeader</a> method to populate the ContentInfo object with the header information.




## -see-also




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>



<a href="https://msdn.microsoft.com/a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a">Initializing the ContentInfo Object of a New ASF File</a>
 

 

