---
UID: NF:strmif.IAMVideoCompression.GetInfo
title: IAMVideoCompression::GetInfo
author: windows-sdk-content
description: The GetInfo method retrieves information about the filter's compression properties, including capabilities and default values.
old-location: dshow\iamvideocompression_getinfo.htm
tech.root: DirectShow
ms.assetid: d8ba2ba2-510a-4fb8-844e-48059ec4ef0d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMVideoCompression interface, IAMVideoCompression interface [DirectShow],GetInfo method, IAMVideoCompression.GetInfo, IAMVideoCompression::GetInfo, IAMVideoCompressionGetInfo, dshow.iamvideocompression_getinfo, strmif/IAMVideoCompression::GetInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression.GetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoCompression::GetInfo


## -description



The <code>GetInfo</code> method retrieves information about the filter's compression properties, including capabilities and default values.




## -parameters




### -param pszVersion [out]

Pointer to a buffer that receives a version string, such as "Version 2.1.0."


### -param pcbVersion [in, out]

Receives the size of the version string, in bytes.


### -param pszDescription [out]

Pointer to a buffer that receives a description string, such as "My Video Compressor."


### -param pcbDescription [in, out]

Receives the size of the description string, in bytes.


### -param pDefaultKeyFrameRate [out]

Receives the default key-frame rate.


### -param pDefaultPFramesPerKey [out]

Receives the default rate of predicted (P) frames per key frame.


### -param pDefaultQuality [out]

Receives the default quality.


### -param pCapabilities [out]

Receives the compression capabilities, as a bitwise combination of zero or more <a href="https://msdn.microsoft.com/e964756f-1c60-42fd-8497-637d5fc005d7">CompressionCaps</a> flags.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Any of the listed parameters can be <b>NULL</b>, in which case the method ignores that parameter.

The application must allocate the buffers for the version and description strings. To determine the required size of the buffers, call this method with <b>NULL</b> for the <i>pszVersion</i> and <i>pszDescription</i> parameters. Use the values returned in <i>pcbVersion</i> and <i>pcbDescription</i> to allocate the buffers and then call the method again, as shown in the following code:


```cpp

// Get the size of the version and description strings, in bytes.
int cbVersion, cbDesc; 
hr = pCompress->GetInfo(NULL, &cbVersion, NULL, &cbDesc, 
    NULL, NULL, NULL, NULL);
if (SUCCEEDED(hr))
{
    // Allocate the buffers.
    WCHAR *pszVersion = new WCHAR[cbVersion / sizeof(WCHAR)];  
    WCHAR *pszDesc = new WCHAR[cbDesc / sizeof(WCHAR)];

    // Now query for the strings.
    hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
        NULL, NULL, NULL, NULL);
    }
    delete [] pszVersion;
    delete [] pszDesc;
}

```


Note that the strings are wide-character strings, and the returned sizes are in bytes, not number of characters. Also, one or both strings might be zero-length.

The <i>pCapabilities</i> parameter receives a set of flags indicating which compression properties are supported, and thus which <b>IAMVideoCompression</b> methods are supported. For example, if the <b>CompressionCaps_CanKeyFrame</b> flag is returned, it the filter supports the <a href="https://msdn.microsoft.com/af73cfaa-3297-44a7-96a7-8805aad057e2">IAMVideoCompression::get_KeyFrameRate</a> and <a href="https://msdn.microsoft.com/dc229333-3524-4228-ab13-a6e9619643fd">IAMVideoCompression::put_KeyFrameRate</a> methods.

The remaining parameters receive default values for the compression properties. For unsupported properties (as determined by the flags returned in <i>pCapabilities</i>), you should ignore the corresponding default value, as it may not be correct or meaningful.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>
 

 

