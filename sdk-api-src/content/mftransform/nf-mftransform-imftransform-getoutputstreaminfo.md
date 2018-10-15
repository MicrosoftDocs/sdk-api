---
UID: NF:mftransform.IMFTransform.GetOutputStreamInfo
title: IMFTransform::GetOutputStreamInfo
author: windows-sdk-content
description: Gets the buffer requirements and other information for an output stream on this Media Foundation transform (MFT).
old-location: mf\imftransform_getoutputstreaminfo.htm
tech.root: medfound
ms.assetid: 06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5, GetOutputStreamInfo, GetOutputStreamInfo method [Media Foundation], GetOutputStreamInfo method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetOutputStreamInfo method, IMFTransform.GetOutputStreamInfo, IMFTransform::GetOutputStreamInfo, mf.imftransform_getoutputstreaminfo, mftransform/IMFTransform::GetOutputStreamInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFTransform.GetOutputStreamInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTransform::GetOutputStreamInfo


## -description


Gets the buffer requirements and other information for an output stream on this Media Foundation transform (MFT).
        


## -parameters




### -param dwOutputStreamID [in]

Output stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/0715c78e-de92-439d-a4f3-078e19f78a8e">IMFTransform::GetStreamIDs</a>.
          


### -param pStreamInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/4181d8b8-7c1b-4f8e-a0c6-63ab039539f6">MFT_OUTPUT_STREAM_INFO</a> structure. The method fills the structure with information about the output stream.
          


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.
              

</td>
</tr>
</table>
 




## -remarks



It is valid to call this method before setting the media types. Note that the results of this call can change dynamically after the media type changes and after <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a> is called, so you may need to call this method again after either of these occur.

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetOutputStreamInfo</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

