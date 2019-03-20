---
UID: NF:mfapi.MFInitMediaTypeFromVideoInfoHeader2
title: MFInitMediaTypeFromVideoInfoHeader2 function (mfapi.h)
author: windows-sdk-content
description: Initializes a media type from a DirectShow VIDEOINFOHEADER2 structure.
old-location: mf\mfinitmediatypefromvideoinfoheader2.htm
tech.root: medfound
ms.assetid: 4077ae40-75b2-4c45-b62e-740e216ebf89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 4077ae40-75b2-4c45-b62e-740e216ebf89, MFInitMediaTypeFromVideoInfoHeader2, MFInitMediaTypeFromVideoInfoHeader2 function [Media Foundation], mf.mfinitmediatypefromvideoinfoheader2, mfapi/MFInitMediaTypeFromVideoInfoHeader2
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
 - MFInitMediaTypeFromVideoInfoHeader2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFInitMediaTypeFromVideoInfoHeader2 function


## -description



Initializes a media type from a DirectShow <b>VIDEOINFOHEADER2</b> structure.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>.


### -param pVIH2

Pointer to a <b>VIDEOINFOHEADER2</b> structure that describes the media type. The caller must fill in the structure members before calling this function.


### -param cbBufSize

Size of the <b>VIDEOINFOHEADER2</b> structure, in bytes.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>VIDEOINFOHEADER2</b> structure.


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




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6aee18b8-79b1-47fb-816f-d1c2c77b3a03">Media Type Conversions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

