---
UID: NF:mfapi.MFInitAMMediaTypeFromMFMediaType
title: MFInitAMMediaTypeFromMFMediaType function
author: windows-sdk-content
description: Initializes a DirectShow AM_MEDIA_TYPE structure from a Media Foundation media type.
old-location: mf\mfinitammediatypefrommfmediatype.htm
tech.root: medfound
ms.assetid: dbb69578-2563-476f-92f4-6b4e2bb2c77a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFInitAMMediaTypeFromMFMediaType, MFInitAMMediaTypeFromMFMediaType function [Media Foundation], dbb69578-2563-476f-92f4-6b4e2bb2c77a, mf.mfinitammediatypefrommfmediatype, mfapi/MFInitAMMediaTypeFromMFMediaType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MFInitAMMediaTypeFromMFMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFInitAMMediaTypeFromMFMediaType
: 
---

# MFInitAMMediaTypeFromMFMediaType function


## -description



Initializes a DirectShow <b>AM_MEDIA_TYPE</b> structure from a Media Foundation media type.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to convert.


### -param guidFormatBlockType

Format type GUID. This value corresponds to the <b>formattype</b> member of the <b>AM_MEDIA_TYPE</b> structure and specifies the type of format block to allocate. If the value is GUID_NULL, the function attempts to deduce the correct format block, based on the major type and subtype.


### -param pAMType

Pointer to an <b>AM_MEDIA_TYPE</b> structure. The function allocates memory for the format block. The caller must release the format block by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> on the <b>pbFormat</b> member.


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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The media type is not valid.

</td>
</tr>
</table>
 




## -remarks



This function can also be used with the following format structures that are equivalent to <b>AM_MEDIA_TYPE</b>:

<ul>
<li><b>DMO_MEDIA_TYPE</b> (DirectX Media Objects)</li>
<li><b>WM_MEDIA_TYPE</b> (Windows Media Format SDK)</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

