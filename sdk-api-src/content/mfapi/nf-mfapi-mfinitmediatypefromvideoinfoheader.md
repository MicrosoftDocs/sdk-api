---
UID: NF:mfapi.MFInitMediaTypeFromVideoInfoHeader
title: MFInitMediaTypeFromVideoInfoHeader function
author: windows-sdk-content
description: Initializes a media type from a DirectShow VIDEOINFOHEADER structure.
old-location: mf\mfinitmediatypefromvideoinfoheader.htm
tech.root: medfound
ms.assetid: 7f88422d-c968-4eea-83cb-45e6cfe37921
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 7f88422d-c968-4eea-83cb-45e6cfe37921, MFInitMediaTypeFromVideoInfoHeader, MFInitMediaTypeFromVideoInfoHeader function [Media Foundation], mf.mfinitmediatypefromvideoinfoheader, mfapi/MFInitMediaTypeFromVideoInfoHeader
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
 - MFInitMediaTypeFromVideoInfoHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFInitMediaTypeFromVideoInfoHeader
: 
---

# MFInitMediaTypeFromVideoInfoHeader function


## -description



Initializes a media type from a DirectShow <b>VIDEOINFOHEADER</b> structure.




## -parameters




### -param pMFType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type to initialize. To create the uninitialized media type object, call <a href="https://msdn.microsoft.com/05b0941e-03ce-4ced-9022-22b65d1c4b4c">MFCreateMediaType</a>.


### -param pVIH

Pointer to a <b>VIDEOINFOHEADER</b> structure that describes the media type. The caller must fill in the structure members before calling this function.


### -param cbBufSize

Size of the <b>VIDEOINFOHEADER</b> structure, in bytes.


### -param pSubtype

Pointer to a subtype GUID. This parameter can be <b>NULL</b>. If the subtype GUID is specified, the function uses it to set the media subtype. Otherwise, the function attempts to deduce the subtype from the <b>biCompression</b> field contained in the <b>VIDEOINFOHEADER</b> structure.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6aee18b8-79b1-47fb-816f-d1c2c77b3a03">Media Type Conversions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

