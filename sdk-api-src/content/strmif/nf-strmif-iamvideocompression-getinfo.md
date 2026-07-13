---
UID: NF:strmif.IAMVideoCompression.GetInfo
title: IAMVideoCompression::GetInfo (strmif.h)
description: The GetInfo method retrieves information about the filter's compression properties, including capabilities and default values.
helpviewer_keywords: ["GetInfo","GetInfo method [DirectShow]","GetInfo method [DirectShow]","IAMVideoCompression interface","IAMVideoCompression interface [DirectShow]","GetInfo method","IAMVideoCompression.GetInfo","IAMVideoCompression::GetInfo","IAMVideoCompressionGetInfo","dshow.iamvideocompression_getinfo","strmif/IAMVideoCompression::GetInfo"]
old-location: dshow\iamvideocompression_getinfo.htm
tech.root: dshow
ms.assetid: d8ba2ba2-510a-4fb8-844e-48059ec4ef0d
ms.date: 4/26/2023
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IAMVideoCompression interface, IAMVideoCompression interface [DirectShow],GetInfo method, IAMVideoCompression.GetInfo, IAMVideoCompression::GetInfo, IAMVideoCompressionGetInfo, dshow.iamvideocompression_getinfo, strmif/IAMVideoCompression::GetInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMVideoCompression::GetInfo
 - strmif/IAMVideoCompression::GetInfo
dev_langs:
 - c++
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
---

# IAMVideoCompression::GetInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

Receives the compression capabilities, as a bitwise combination of zero or more <a href="/windows/desktop/api/strmif/ne-strmif-compressioncaps">CompressionCaps</a> flags.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Any of the listed parameters can be <b>NULL</b>, in which case the method ignores that parameter.

The application must allocate the buffers for the version and description strings. To determine the required size of the buffers, call this method with <b>NULL</b> for the <i>pszVersion</i> and <i>pszDescription</i> parameters. Use the values returned in <i>pcbVersion</i> and <i>pcbDescription</i> to allocate the buffers and then call the method again, as shown in the following code:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>

```
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
</td>
</tr>
</table></span></div>
Note that the strings are wide-character strings, and the returned sizes are in bytes, not number of characters. Also, one or both strings might be zero-length.

The <i>pCapabilities</i> parameter receives a set of flags indicating which compression properties are supported, and thus which <b>IAMVideoCompression</b> methods are supported. For example, if the <b>CompressionCaps_CanKeyFrame</b> flag is returned, it the filter supports the <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_keyframerate">IAMVideoCompression::get_KeyFrameRate</a> and <a href="/windows/desktop/api/strmif/nf-strmif-iamvideocompression-put_keyframerate">IAMVideoCompression::put_KeyFrameRate</a> methods.

The remaining parameters receive default values for the compression properties. For unsupported properties (as determined by the flags returned in <i>pCapabilities</i>), you should ignore the corresponding default value, as it may not be correct or meaningful.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>