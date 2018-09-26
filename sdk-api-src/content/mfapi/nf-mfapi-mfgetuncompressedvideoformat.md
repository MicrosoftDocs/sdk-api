---
UID: NF:mfapi.MFGetUncompressedVideoFormat
title: MFGetUncompressedVideoFormat function
author: windows-sdk-content
description: Returns the FOURCC or D3DFORMAT value for an uncompressed video format.
old-location: mf\mfgetuncompressedvideoformat.htm
tech.root: medfound
ms.assetid: 7869025a-dacf-47e6-b129-db5b2daefa3b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 7869025a-dacf-47e6-b129-db5b2daefa3b, MFGetUncompressedVideoFormat, MFGetUncompressedVideoFormat function [Media Foundation], mf.mfgetuncompressedvideoformat, mfapi/MFGetUncompressedVideoFormat
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
req.lib: Evr.lib
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
 - MFGetUncompressedVideoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetUncompressedVideoFormat function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>.]

Returns the FOURCC or <b>D3DFORMAT</b> value for an uncompressed video format.


## -parameters




### -param pVideoFormat [in]

Pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.
          


## -returns



Returns a FOURCC or <b>D3DFORMAT</b> value that identifies the video format. If the video format is compressed or not recognized, the return value is D3DFMT_UNKNOWN.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

