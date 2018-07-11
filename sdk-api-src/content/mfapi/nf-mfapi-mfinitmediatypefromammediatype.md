---
UID: NF:mfapi.MFInitMediaTypeFromAMMediaType
title: MFInitMediaTypeFromAMMediaType function
author: windows-sdk-content
description: Initializes a media type from a DirectShow AM_MEDIA_TYPE structure.
old-location: mf\mfinitmediatypefromammediatype.htm
old-project: medfound
ms.assetid: da5dcc32-c027-4b9a-b72f-a60b98885636
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: MFInitMediaTypeFromAMMediaType, MFInitMediaTypeFromAMMediaType function [Media Foundation], da5dcc32-c027-4b9a-b72f-a60b98885636, mf.mfinitmediatypefromammediatype, mfapi/MFInitMediaTypeFromAMMediaType
ms.prod: windows
ms.technology: windows-sdk
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
 - MFInitMediaTypeFromAMMediaType
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFInitMediaTypeFromAMMediaType function


## -description



Initializes a media type from a DirectShow <b>AM_MEDIA_TYPE</b> structure.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>.


### -param pAMType

Pointer to an <b>AM_MEDIA_TYPE</b> structure that describes the media type. The caller must fill in the structure members before calling this function.


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
 

 

