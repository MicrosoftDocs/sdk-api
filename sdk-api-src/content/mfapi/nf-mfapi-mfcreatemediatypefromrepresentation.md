---
UID: NF:mfapi.MFCreateMediaTypeFromRepresentation
title: MFCreateMediaTypeFromRepresentation function (mfapi.h)
author: windows-sdk-content
description: Creates a Media Foundation media type from another format representation.
old-location: mf\mfcreatemediatypefromrepresentation.htm
tech.root: medfound
ms.assetid: 5d85c47e-2e40-45f2-8f17-52f642652112
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5d85c47e-2e40-45f2-8f17-52f642652112, MFCreateMediaTypeFromRepresentation, MFCreateMediaTypeFromRepresentation function [Media Foundation], mf.mfcreatemediatypefromrepresentation, mfapi/MFCreateMediaTypeFromRepresentation
ms.topic: function
f1_keywords: 
 - "mfapi/MFCreateMediaTypeFromRepresentation"
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
 - MFCreateMediaTypeFromRepresentation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMediaTypeFromRepresentation function


## -description



Creates a Media Foundation media type from another format representation.




## -parameters




### -param guidRepresentation [in]

GUID that specifies which format representation to convert. The following value is defined.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td>AM_MEDIA_TYPE_REPRESENTATION</td>
<td>Convert a DirectShow <b>AM_MEDIA_TYPE</b> structure.</td>
</tr>
</table>
 


### -param pvRepresentation [in]

Pointer to a buffer that contains the format representation to convert. The layout of the buffer depends on the value of <i>guidRepresentation</i>.


### -param ppIMediaType [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_REPRESENTATION</b></dt>
</dl>
</td>
<td width="60%">
The GUID specified in <i>guidRepresentation</i> is not supported.

</td>
</tr>
</table>
 




## -remarks



If the original format is a DirectShow audio media type, and the format type is not recognized, the function sets the following attributes on the converted media type.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-am-format-type-attribute">MF_MT_AM_FORMAT_TYPE</a>
</td>
<td>Contains the format type GUID.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-mt-user-data-attribute">MF_MT_USER_DATA</a>
</td>
<td>Contains the format block.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

