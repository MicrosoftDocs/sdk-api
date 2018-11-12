---
UID: NF:wmcontainer.IMFASFContentInfo.GenerateHeader
title: IMFASFContentInfo::GenerateHeader
author: windows-sdk-content
description: Encodes the data in the MFASFContentInfo object into a binary Advanced Systems Format (ASF) header.
old-location: mf\imfasfcontentinfo_generateheader.htm
tech.root: medfound
ms.assetid: 972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 972f5ae7-ad00-4c3b-8ec4-2cef4ce03c4e, GenerateHeader, GenerateHeader method [Media Foundation], GenerateHeader method [Media Foundation],IMFASFContentInfo interface, IMFASFContentInfo interface [Media Foundation],GenerateHeader method, IMFASFContentInfo.GenerateHeader, IMFASFContentInfo::GenerateHeader, mf.imfasfcontentinfo_generateheader, wmcontainer/IMFASFContentInfo::GenerateHeader
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
 - IMFASFContentInfo.GenerateHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFContentInfo::GenerateHeader


## -description



Encodes the data in the <b>MFASFContentInfo</b> object into a binary Advanced Systems Format (ASF) header.




## -parameters




### -param pIHeader [in, out]

A pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of the buffer object that will receive the encoded header. Set to <b>NULL</b> to retrieve the size of the header.
          


### -param pcbHeader [out]

Size of the encoded ASF header in bytes. If <i>pIHeader</i> is <b>NULL</b>, this value is set to the buffer size required to hold the encoded header.
          


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The ASF Header Objects do not exist for the media that the ContentInfo object holds reference to.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ASF_INVALIDDATA</b></dt>
</dl>
</td>
<td width="60%">
The ASF Header Object size exceeds 10 MB.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed in <i>pIHeader</i> is not large enough to hold the ASF Header Object information.
              

</td>
</tr>
</table>
 




## -remarks



The size received in the <i>pcbHeader</i> parameter includes the padding size. The content information shrinks or expands the padding data depending on the size of the ASF Header Objects.

During this call, the stream properties are set based on the encoding properties of the profile. These properties are available through the <a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a>



<a href="https://msdn.microsoft.com/cf73306d-156a-45c0-a3d6-ae48734f5709">Generating a New ASF Header Object</a>



<a href="https://msdn.microsoft.com/9f490e6a-f378-45c1-a69d-985c6e884358">IMFASFContentInfo</a>
 

 

