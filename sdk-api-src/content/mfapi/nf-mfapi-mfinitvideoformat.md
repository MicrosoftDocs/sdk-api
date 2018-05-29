---
UID: NF:mfapi.MFInitVideoFormat
title: MFInitVideoFormat function
author: windows-sdk-content
description: Initializes an MFVIDEOFORMAT structure for a standard video format such as DVD, analog television, or ATSC digital television.
old-location: mf\mfinitvideoformat.htm
old-project: medfound
ms.assetid: 1cb47f95-cdb6-4998-9980-2f22e282df11
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 1cb47f95-cdb6-4998-9980-2f22e282df11, MFInitVideoFormat, MFInitVideoFormat function [Media Foundation], mf.mfinitvideoformat, mfapi/MFInitVideoFormat
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFInitVideoFormat
product: Windows
targetos: Windows
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFInitVideoFormat function


## -description


<p class="CCE_Message">[This API is not supported and may be altered or unavailable in the future. Applications should avoid using the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure, and use media type attributes instead. For more information, see <a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>.]


          Initializes an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure for a standard video format such as DVD, analog television, or ATSC digital television.


## -parameters




### -param pVideoFormat [out]


            A pointer to an <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure. The function fills in the structure members based on the video format specified in the type parameter.
          


### -param type [in]


            The video format, specified as a member of the <a href="https://msdn.microsoft.com/559ea2e9-308b-428a-ae24-bf3fdc27e24e">MFStandardVideoFormat</a> enumeration.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="media_foundation_headers_and_libraries.htm">Library Changes in Windows 7</a>.</div>
<div> </div>

#### Examples

The following example creates a media type object for a standard video format. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Creates a media type for a standard video format.
HRESULT CreateStandardVideoMediaType(MFStandardVideoFormat type, IMFMediaType **ppMediaType)
{
    IMFMediaType *pMediaType = NULL;

    MFVIDEOFORMAT format;

    // Fill in the MFVIDEOFORMAT structure for the video format.
    HRESULT hr = MFInitVideoFormat(&amp;format, type);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a new (empty) media type.
    hr = MFCreateMediaType(&amp;pMediaType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the media type from the MFVIDEOFORMAT structure.
    hr = MFInitMediaTypeFromMFVideoFormat(pMediaType, &amp;format, sizeof(format));
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppMediaType = pMediaType;
    (*ppMediaType)-&gt;AddRef();

done:
    SafeRelease(&amp;pMediaType);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

