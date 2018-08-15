---
UID: NF:mfapi.MFCreateAMMediaTypeFromMFMediaType
title: MFCreateAMMediaTypeFromMFMediaType function
author: windows-sdk-content
description: Creates a DirectShow AM_MEDIA_TYPE structure from a Media Foundation media type.
old-location: mf\mfcreateammediatypefrommfmediatype.htm
old-project: medfound
ms.assetid: 53b191d4-89b3-4b16-8f89-50f256689e85
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 53b191d4-89b3-4b16-8f89-50f256689e85, MFCreateAMMediaTypeFromMFMediaType, MFCreateAMMediaTypeFromMFMediaType function [Media Foundation], mf.mfcreateammediatypefrommfmediatype, mfapi/MFCreateAMMediaTypeFromMFMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateAMMediaTypeFromMFMediaType
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateAMMediaTypeFromMFMediaType function


## -description



Creates a DirectShow <b>AM_MEDIA_TYPE</b> structure from a Media Foundation media type.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to convert.


### -param guidFormatBlockType

Format type GUID. This value corresponds to the <b>formattype</b> member of the <b>AM_MEDIA_TYPE</b> structure and specifies the type of format block to allocate. If the value is GUID_NULL, the function attempts to deduce the correct format block, based on the major type and subtype.


### -param ppAMType

Receives a pointer to an <b>AM_MEDIA_TYPE</b> structure. The caller must release the memory allocated for the structure by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. The function also allocates memory for the format block, which the caller must release by calling <b>CoTaskMemFree</b> on the <b>pbFormat</b> member.


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
 




## -remarks



This function can also be used with the following format structures that are equivalent to <b>AM_MEDIA_TYPE</b>:

<ul>
<li>
<b>DMO_MEDIA_TYPE</b> (DirectX Media Objects)

</li>
<li>
<b>WM_MEDIA_TYPE</b> (Windows Media Format SDK)

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6aee18b8-79b1-47fb-816f-d1c2c77b3a03">Media Type Conversions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

