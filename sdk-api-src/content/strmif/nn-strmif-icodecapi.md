---
UID: NN:strmif.ICodecAPI
title: ICodecAPI (strmif.h)
description: The ICodecAPI interface (strmif.h) sets and retrieves settings on an encoder or decoder filter.
helpviewer_keywords: ["ICodecAPI","ICodecAPI interface [DirectShow]","ICodecAPI interface [DirectShow]","described","ICodecAPIInterface","dshow.icodecapi","strmif/ICodecAPI"]
old-location: dshow\icodecapi.htm
tech.root: dshow
ms.assetid: cc3f1bd9-1d36-45e6-94e2-07f2800fd073
ms.date: 4/26/2023
ms.keywords: ICodecAPI, ICodecAPI interface [DirectShow], ICodecAPI interface [DirectShow],described, ICodecAPIInterface, dshow.icodecapi, strmif/ICodecAPI
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
 - ICodecAPI
 - strmif/ICodecAPI
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
 - ICodecAPI
---

# ICodecAPI interface


## -description

\[The usage of the CodecAPI feature with [DirectShow](/windows/win32/directshow/directshow) is no longer recommended. DirectShow usage has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 11 and Windows 10. Instead of **DirectShow**, Microsoft strongly recommends when possible that new code use **MediaPlayer**, **IMFMediaEngine**, and **Audio/Video Capture in Media Foundation**. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ICodecAPI</b> interface sets and retrieves settings on an encoder or decoder filter.

> [!Note]
> APIs declared in strmif.h are not supported for Universal Windows Platform (UWP) apps. To use ICodecAPI in a UWP app, use the version declared in [icodecapi.h](/windows/win32/api/icodecapi/). 

## -inheritance

The <b>ICodecAPI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICodecAPI</b> also has these types of members:

## -remarks

This interface defines a generic mechanism for setting properties on a codec (encoder or decoder). A <i>codec property</i> is a key/value pair, where the key is a GUID and the value is a <b>VARIANT</b>. The interpretation of the <b>VARIANT</b> data depends on the property GUID. For a list of codec property GUIDs, see <a href="/windows/desktop/DirectShow/codec-api-properties">Codec API Properties</a>.

<h3><a id="Codec_Profiles"></a><a id="codec_profiles"></a><a id="CODEC_PROFILES"></a>Codec Profiles</h3>
Codecs can optionally store profile and capability information in the system registry. This information enables applications to query the device during device enumeration. Default profiles are stored in the following registry key:<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Classes</b>
         <b>CLSID</b>
            <b><i>Category</i></b>
               <b>Profiles</b></pre>Each profile is a registry key whose default string is a text description of the profile. Each value has a GUID name, followed by a string value containing the numeric GUID value. For example:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
  HLKM\Software\Classes\CLSID\&lt;category&gt;\Profiles\DVD
    default "HQ DVD"
    REG_SZ {...} = "0"
    REG_SZ {...} = "1234"
</pre>
</td>
</tr>
</table></span></div>
where {...} is a property GUID that the application can map into its user interface. Microsoft is currently considering the definition of a set of standard profiles.

Default codec capabilities are stored under HLKM\Software\Classes\CLSID\&lt;category&gt;\Instance\&lt;Filter CLSID&gt;\Capabilities. Each value has a GUID name, followed by a string value containing the numeric GUID value. For example:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HLKM\Software\Classes\CLSID\&lt;category&gt;\Instance\&lt;My DVD encoder&gt;\Capabilities
     default "My DVD encoder"
     REG_SZ_MULTI {...}
</pre>
</td>
</tr>
</table></span></div>
where {...} is a property GUID that the application can map into its user interface.

## -see-also

* [D3D12 video encoding](https://learn.microsoft.com/en-us/windows-hardware/drivers/display/video-encoding-d3d12)
* [Announcing new DirectX 12 feature – Video Encoding!](https://devblogs.microsoft.com/directx/announcing-new-directx-12-feature-video-encoding/)
