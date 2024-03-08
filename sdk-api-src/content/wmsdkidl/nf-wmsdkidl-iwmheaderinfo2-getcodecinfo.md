---
UID: NF:wmsdkidl.IWMHeaderInfo2.GetCodecInfo
title: IWMHeaderInfo2::GetCodecInfo (wmsdkidl.h)
description: The GetCodecInfo method retrieves information about a codec that is used to create the content of a file.
helpviewer_keywords: ["GetCodecInfo","GetCodecInfo method [windows Media Format]","GetCodecInfo method [windows Media Format]","IWMHeaderInfo2 interface","GetCodecInfo method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo2 interface [windows Media Format]","GetCodecInfo method","IWMHeaderInfo2.GetCodecInfo","IWMHeaderInfo2::GetCodecInfo","IWMHeaderInfo2GetCodecInfo","IWMHeaderInfo3 interface [windows Media Format]","GetCodecInfo method","IWMHeaderInfo3::GetCodecInfo","wmformat.iwmheaderinfo2_getcodecinfo","wmsdkidl/IWMHeaderInfo2::GetCodecInfo","wmsdkidl/IWMHeaderInfo3::GetCodecInfo"]
old-location: wmformat\iwmheaderinfo2_getcodecinfo.htm
tech.root: wmformat
ms.assetid: 685eaf9e-6cc8-4c38-be34-afa4b504a326
ms.date: 4/26/2023
ms.keywords: GetCodecInfo, GetCodecInfo method [windows Media Format], GetCodecInfo method [windows Media Format],IWMHeaderInfo2 interface, GetCodecInfo method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo2 interface [windows Media Format],GetCodecInfo method, IWMHeaderInfo2.GetCodecInfo, IWMHeaderInfo2::GetCodecInfo, IWMHeaderInfo2GetCodecInfo, IWMHeaderInfo3 interface [windows Media Format],GetCodecInfo method, IWMHeaderInfo3::GetCodecInfo, wmformat.iwmheaderinfo2_getcodecinfo, wmsdkidl/IWMHeaderInfo2::GetCodecInfo, wmsdkidl/IWMHeaderInfo3::GetCodecInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMHeaderInfo2::GetCodecInfo
 - wmsdkidl/IWMHeaderInfo2::GetCodecInfo
dev_langs:
 - c++
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
 - qasf.dll
api_name:
 - IWMHeaderInfo2.GetCodecInfo
 - IWMHeaderInfo3.GetCodecInfo
---

# IWMHeaderInfo2::GetCodecInfo


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecInfo</b> method retrieves information about a codec that is used to create the content of a file.

## -parameters

### -param wIndex [in]

<b>DWORD</b> that contains the zero-based codec index.

### -param pcchName [in, out]

On input, pointer to the length of <i>pwszName</i> in wide characters. On output, pointer to a count of the characters that are used in <i>pwszName</i>.This includes the terminating <b>null</b> character.

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the name of the codec is copied.

### -param pcchDescription [in, out]

On input, pointer to the length of <i>pwszDescription</i> in wide characters. On output, pointer to a count of the characters that are used in <i>pwszDescription</i>. This includes the terminating <b>null</b> character.

### -param pwszDescription [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the description of the codec is copied.

### -param pCodecType [out]

Pointer to one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_codec_info_type">WMT_CODEC_INFO_TYPE</a> enumeration type.

### -param pcbCodecInfo [in, out]

On input, pointer to the length of <i>pbCodecInfo</i>, in bytes. On output, pointer to a count of the bytes used in <i>pbCodecInfo</i>.

### -param pbCodecInfo [out]

Pointer to a byte array.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

You should make two calls to <b>GetCodecInfo</b>. On the first call, pass <b>NULL</b> for <i>pwszName</i>, <i>pwszDescription</i>, and <i>pbCodecInfo</i>. On return the values pointed to by <i>pcchName</i> and <i>pcchDescription</i> are set to the number of characters. These include the terminating <b>null</b> character, which is required to hold the name string in <i>pcchName</i> and the description string in <i>pcchDescription</i>. The value pointed to by <i>pcbCodecInfo</i> is set to the buffer size required to hold the codec information. With these sizes, you can allocate the required amount of memory to receive each value. Pass pointers to the buffers are <i>pwszName</i>, <i>pwszDescription</i>, and <i>pbCodecInfo</i> on the second call.

Use this method, and the <b>GetCodecInfoCount</b> method, to enumerate through the codec information.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount">IWMHeaderInfo2::GetCodecInfoCount</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_codec_info_type">WMT_CODEC_INFO_TYPE</a>