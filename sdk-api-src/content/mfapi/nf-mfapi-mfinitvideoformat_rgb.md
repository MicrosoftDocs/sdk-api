---
UID: NF:mfapi.MFInitVideoFormat_RGB
title: MFInitVideoFormat_RGB function
author: windows-sdk-content
description: Initializes an MFVIDEOFORMAT structure for an uncompressed RGB video format.
old-location: mf\mfinitvideoformat_rgb.htm
tech.root: medfound
ms.assetid: 4c437f26-6fe1-477d-9955-bc900215aa59
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 4c437f26-6fe1-477d-9955-bc900215aa59, MFInitVideoFormat_RGB, MFInitVideoFormat_RGB function [Media Foundation], mf.mfinitvideoformat_rgb, mfapi/MFInitVideoFormat_RGB
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
 - MFInitVideoFormat_RGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFInitVideoFormat_RGB function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>.]

Initializes an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure for an uncompressed RGB video format.


## -parameters




### -param pVideoFormat [in]

A pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure. The functions fills in the structure members with the format information.
          


### -param dwWidth [in]

The width of the video, in pixels.
          


### -param dwHeight [in]

The height of the video, in pixels.
          


### -param D3Dfmt [in]

A 
            
              <b>D3DFORMAT</b> value that specifies the RGB format.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function fills in some reasonable default values for the specified RGB format.
      

Developers are encouraged to use media type attributes instead of using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure. See <a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>.
      

In general, you should avoid calling this function. If you know all of the format details, you can fill in the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure without this function. If you do not know all of the format details, attributes are preferable to using the <b>MFVIDEOFORMAT</b> structure.
      

<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>



<a href="https://msdn.microsoft.com/50bf2947-27ee-4092-9d3a-a1c13ee80e95">Uncompressed Video Media Types</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

