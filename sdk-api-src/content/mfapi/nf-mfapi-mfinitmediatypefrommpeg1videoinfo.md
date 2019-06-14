---
UID: NF:mfapi.MFInitMediaTypeFromMPEG1VideoInfo
title: MFInitMediaTypeFromMPEG1VideoInfo function (mfapi.h)
author: windows-sdk-content
description: Initializes a media type from a DirectShow MPEG1VIDEOINFO structure.
old-location: mf\mfinitmediatypefrommpeg1videoinfo.htm
tech.root: medfound
ms.assetid: 2506ae6e-a3bb-4d36-8c70-837a42cfb272
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2506ae6e-a3bb-4d36-8c70-837a42cfb272, MFInitMediaTypeFromMPEG1VideoInfo, MFInitMediaTypeFromMPEG1VideoInfo function [Media Foundation], mf.mfinitmediatypefrommpeg1videoinfo, mfapi/MFInitMediaTypeFromMPEG1VideoInfo
ms.topic: function
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFInitMediaTypeFromMPEG1VideoInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFInitMediaTypeFromMPEG1VideoInfo function


## -description



Initializes a media type from a DirectShow <b>MPEG1VIDEOINFO</b> structure.




## -parameters




### -param pMFType

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>.


### -param pMP1VI

Pointer to a <b>MPEG1VIDEOINFO</b> structure that describes the media type. The caller must fill in the structure members before calling this function.


### -param cbBufSize

Size of the <b>MPEG1VIDEOINFO</b> structure, in bytes.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>MPEG1VIDEOINFO</b> structure.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-type-conversions">Media Type Conversions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-types">Media Types</a>
 

 

