---
UID: NF:wmsdkidl.IWMCodecInfo.GetCodecFormat
title: IWMCodecInfo::GetCodecFormat
author: windows-sdk-content
description: The GetCodecFormat method retrieves one format supported by a specified codec. This method retrieves a pointer to the IWMStreamConfig interface of a stream configuration object containing the stream settings for the supported format.
old-location: wmformat\iwmcodecinfo_getcodecformat.htm
old-project: wmformat
ms.assetid: dbfffc96-2286-4fdf-a76f-ad8e0ecd7aff
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCodecFormat, GetCodecFormat method [windows Media Format], GetCodecFormat method [windows Media Format],IWMCodecInfo interface, IWMCodecInfo interface [windows Media Format],GetCodecFormat method, IWMCodecInfo.GetCodecFormat, IWMCodecInfo::GetCodecFormat, IWMCodecInfoGetCodecFormat, wmformat.iwmcodecinfo_getcodecformat, wmsdkidl/IWMCodecInfo::GetCodecFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecInfo::GetCodecFormat


## -description



The <b>GetCodecFormat</b> method retrieves one format supported by a specified codec. This method retrieves a pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of a stream configuration object containing the stream settings for the supported format.




## -parameters




### -param guidType [in]

<b>GUID</b> identifying the major type of digital media. This must be one of the following constants.

<table>
<tr>
<th>
                  Constant
                </th>
<th>
                  Description
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

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major type, use the <a href="https://msdn.microsoft.com/873f8d03-5d7b-424c-91f3-e7c8156565be">IWMCodecInfo::GetCodecInfoCount</a> method.


### -param dwFormatIndex [in]

<b>DWORD</b> containing the format index ranging from zero to one less than the number of supported formats. To retrieve the number of individual formats supported by a codec, use the <a href="https://msdn.microsoft.com/b93bfb01-4179-4a0b-bca0-92b1a9a8e605">IWMCodecInfo::GetCodecFormatCount</a> method.


### -param ppIStreamConfig [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig</a> interface of a stream configuration object containing the settings of the specified format.


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

The codec format describes the characteristics of the compressed data stream in the file, and has no direct correlation to the uncompressed format of the input media or the output media. The format of input media data is determined at the time of encoding, using the <a href="https://msdn.microsoft.com/15084a4d-06e8-4f74-9697-ced794d2cdae">IWMWriter::SetInputProps</a> method. The format of output media data is determined at the time of decoding, using the <b>SetOutputProps</b> method of either the <a href="https://msdn.microsoft.com/e995b707-d388-4ec3-b3c8-b111628c13d7">IWMReader</a> interface or the <a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader</a> interface.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.

The Windows Media Video codecs all support a single format that you must complete with your desired settings. When obtaining a video format, you can always use format index 1. For more information see <a href="https://msdn.microsoft.com/caffdfc1-3c35-4b7b-8643-5a9095cc11f6">Configuring Video Streams</a>.




## -see-also




<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo Interface</a>



<a href="https://msdn.microsoft.com/b93bfb01-4179-4a0b-bca0-92b1a9a8e605">IWMCodecInfo::GetCodecFormatCount</a>



<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>
 

 

