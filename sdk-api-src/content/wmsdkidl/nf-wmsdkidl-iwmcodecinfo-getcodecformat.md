---
UID: NF:wmsdkidl.IWMCodecInfo.GetCodecFormat
title: IWMCodecInfo::GetCodecFormat (wmsdkidl.h)
description: The GetCodecFormat method retrieves one format supported by a specified codec. This method retrieves a pointer to the IWMStreamConfig interface of a stream configuration object containing the stream settings for the supported format.
helpviewer_keywords: ["GetCodecFormat","GetCodecFormat method [windows Media Format]","GetCodecFormat method [windows Media Format]","IWMCodecInfo interface","IWMCodecInfo interface [windows Media Format]","GetCodecFormat method","IWMCodecInfo.GetCodecFormat","IWMCodecInfo::GetCodecFormat","IWMCodecInfoGetCodecFormat","wmformat.iwmcodecinfo_getcodecformat","wmsdkidl/IWMCodecInfo::GetCodecFormat"]
old-location: wmformat\iwmcodecinfo_getcodecformat.htm
tech.root: wmformat
ms.assetid: dbfffc96-2286-4fdf-a76f-ad8e0ecd7aff
ms.date: 12/05/2018
ms.keywords: GetCodecFormat, GetCodecFormat method [windows Media Format], GetCodecFormat method [windows Media Format],IWMCodecInfo interface, IWMCodecInfo interface [windows Media Format],GetCodecFormat method, IWMCodecInfo.GetCodecFormat, IWMCodecInfo::GetCodecFormat, IWMCodecInfoGetCodecFormat, wmformat.iwmcodecinfo_getcodecformat, wmsdkidl/IWMCodecInfo::GetCodecFormat
f1_keywords:
- wmsdkidl/IWMCodecInfo.GetCodecFormat
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMCodecInfo.GetCodecFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecInfo::GetCodecFormat


## -description



The <b>GetCodecFormat</b> method retrieves one format supported by a specified codec. This method retrieves a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of a stream configuration object containing the stream settings for the supported format.




## -parameters




### -param guidType [in]

<b>GUID</b> identifying the major type of digital media. This must be one of the following constants.

<table>
<tr>
<th>Constant
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMMEDIATYPE_Video</td>
<td>Specifies a video codec.</td>
</tr>
<tr>
<td>WMMEDIATYPE_Audio</td>
<td>Specifies an audio codec.</td>
</tr>
</table>
 


### -param dwCodecIndex [in]

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major type, use the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecinfocount">IWMCodecInfo::GetCodecInfoCount</a> method.


### -param dwFormatIndex [in]

<b>DWORD</b> containing the format index ranging from zero to one less than the number of supported formats. To retrieve the number of individual formats supported by a codec, use the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount">IWMCodecInfo::GetCodecFormatCount</a> method.


### -param ppIStreamConfig [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of a stream configuration object containing the settings of the specified format.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid or null value has been passed in.

</td>
</tr>
</table>
 




## -remarks



Use this method along with <b>GetCodecFormatCount</b> to enumerate the formats supported by the codec.

The codec format describes the characteristics of the compressed data stream in the file, and has no direct correlation to the uncompressed format of the input media or the output media. The format of input media data is determined at the time of encoding, using the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops">IWMWriter::SetInputProps</a> method. The format of output media data is determined at the time of decoding, using the <b>SetOutputProps</b> method of either the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader</a> interface or the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader</a> interface.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.

The Windows Media Video codecs all support a single format that you must complete with your desired settings. When obtaining a video format, you can always use format index 1. For more information see <a href="https://docs.microsoft.com/windows/desktop/wmformat/configuring-video-streams">Configuring Video Streams</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount">IWMCodecInfo::GetCodecFormatCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>
 

 

