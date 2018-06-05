---
UID: NF:wmsdkidl.IWMCodecInfo.GetCodecFormatCount
title: IWMCodecInfo::GetCodecFormatCount
author: windows-sdk-content
description: The GetCodecFormatCount method retrieves the number of formats supported by the specified codec. Each codec format is a stream configuration that is valid for use with the codec.
old-location: wmformat\iwmcodecinfo_getcodecformatcount.htm
old-project: wmformat
ms.assetid: b93bfb01-4179-4a0b-bca0-92b1a9a8e605
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetCodecFormatCount, GetCodecFormatCount method [windows Media Format], GetCodecFormatCount method [windows Media Format],IWMCodecInfo interface, IWMCodecInfo interface [windows Media Format],GetCodecFormatCount method, IWMCodecInfo.GetCodecFormatCount, IWMCodecInfo::GetCodecFormatCount, IWMCodecInfoGetCodecFormatCount, wmformat.iwmcodecinfo_getcodecformatcount, wmsdkidl/IWMCodecInfo::GetCodecFormatCount
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMCodecInfo.GetCodecFormatCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecInfo::GetCodecFormatCount


## -description



The <b>GetCodecFormatCount</b> method retrieves the number of formats supported by the specified codec. Each codec format is a stream configuration that is valid for use with the codec.




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

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major media type, use the <a href="https://msdn.microsoft.com/873f8d03-5d7b-424c-91f3-e7c8156565be">IWMCodecInfo::GetCodecInfoCount</a> method.


### -param pcFormat [out]

Pointer to a count of the formats supported by the codec.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcFormat</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Other unspecified failure.

</td>
</tr>
</table>
 




## -remarks



Use this method along with <b>GetCodecFormat</b> to enumerate the formats supported by the codec.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.

You do not need to call this method for the Windows Media Video codecs; each video codec supports only a single format. For more information see <a href="https://msdn.microsoft.com/caffdfc1-3c35-4b7b-8643-5a9095cc11f6">Configuring Video Streams</a>.




## -see-also




<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo Interface</a>



<a href="https://msdn.microsoft.com/dbfffc96-2286-4fdf-a76f-ad8e0ecd7aff">IWMCodecInfo::GetCodecFormat</a>
 

 

