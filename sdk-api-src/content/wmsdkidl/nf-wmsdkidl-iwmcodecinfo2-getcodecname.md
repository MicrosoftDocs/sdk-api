---
UID: NF:wmsdkidl.IWMCodecInfo2.GetCodecName
title: IWMCodecInfo2::GetCodecName
author: windows-sdk-content
description: The GetCodecName method retrieves the name of a specified codec.
old-location: wmformat\iwmcodecinfo2_getcodecname.htm
old-project: wmformat
ms.assetid: 4ec4e242-9726-4fac-8867-cb4b13c4cbdc
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetCodecName, GetCodecName method [windows Media Format], GetCodecName method [windows Media Format],IWMCodecInfo2 interface, IWMCodecInfo2 interface [windows Media Format],GetCodecName method, IWMCodecInfo2.GetCodecName, IWMCodecInfo2::GetCodecName, IWMCodecInfo2GetCodecName, wmformat.iwmcodecinfo2_getcodecname, wmsdkidl/IWMCodecInfo2::GetCodecName
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
 - IWMCodecInfo2.GetCodecName
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecInfo2::GetCodecName


## -description



The <b>GetCodecName</b> method retrieves the name of a specified codec.




## -parameters




### -param guidType [in]

GUID identifying the major type of digital media. This must be one of the following constants.

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


### -param wszName [out]

Pointer to a wide-character <b>null</b>-terminated string that receives the codec name.


### -param pcchName [in, out]

On input, pointer to a <b>DWORD</b> containing the size, in wide characters, of the buffer <i>wszName</i>. On output, pointer to a variable containing the number of characters in <i>wszName</i>, including the terminating <b>null</b> character.


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
An invalid or <b>null</b> value has been passed in.

</td>
</tr>
</table>
 




## -remarks



You should make two calls to <b>GetCodecName</b>. On the first call, pass <b>NULL</b> as <i>wszName</i>. On return, the value at <i>pcchName</i> will be set to the buffer size required to hold the codec name, including the terminating character. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>wszName</i> on the second call.




## -see-also




<a href="https://msdn.microsoft.com/0cfb355e-af68-400d-aa64-57f17e7d936b">IWMCodecInfo2 Interface</a>
 

 

