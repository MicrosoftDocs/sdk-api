---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetMaxSpeedFactor
title: IWMReaderAdvanced4::GetMaxSpeedFactor (wmsdkidl.h)
description: The GetMaxSpeedFactor method retrieves the maximum playback rate that can be delivered by the source. For network content, this value reflects the available bandwidth relative to the maximum bit rate of the content.
helpviewer_keywords: ["GetMaxSpeedFactor","GetMaxSpeedFactor method [windows Media Format]","GetMaxSpeedFactor method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","GetMaxSpeedFactor method","IWMReaderAdvanced4.GetMaxSpeedFactor","IWMReaderAdvanced4::GetMaxSpeedFactor","IWMReaderAdvanced4GetMaxSpeedFactor","wmformat.iwmreaderadvanced4_getmaxspeedfactor","wmsdkidl/IWMReaderAdvanced4::GetMaxSpeedFactor"]
old-location: wmformat\iwmreaderadvanced4_getmaxspeedfactor.htm
tech.root: wmformat
ms.assetid: 5617304f-30ed-4072-a0d7-28463ef90a10
ms.date: 4/26/2023
ms.keywords: GetMaxSpeedFactor, GetMaxSpeedFactor method [windows Media Format], GetMaxSpeedFactor method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetMaxSpeedFactor method, IWMReaderAdvanced4.GetMaxSpeedFactor, IWMReaderAdvanced4::GetMaxSpeedFactor, IWMReaderAdvanced4GetMaxSpeedFactor, wmformat.iwmreaderadvanced4_getmaxspeedfactor, wmsdkidl/IWMReaderAdvanced4::GetMaxSpeedFactor
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderAdvanced4::GetMaxSpeedFactor
 - wmsdkidl/IWMReaderAdvanced4::GetMaxSpeedFactor
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
api_name:
 - IWMReaderAdvanced4.GetMaxSpeedFactor
---

# IWMReaderAdvanced4::GetMaxSpeedFactor


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMaxSpeedFactor</b> method retrieves the maximum playback rate that can be delivered by the source. For network content, this value reflects the available bandwidth relative to the maximum bit rate of the content.

## -parameters

### -param pdblFactor [out]

Pointer to a variable that receives the maximum playback rate.

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
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

If the server is using Fast Cache streaming, this method returns 1.0. For local files, including cached content, the method returns DBL_MAX. If no file is open, the method returns 0.0.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache">IWMReaderAdvanced4::IsUsingFastCache</a>