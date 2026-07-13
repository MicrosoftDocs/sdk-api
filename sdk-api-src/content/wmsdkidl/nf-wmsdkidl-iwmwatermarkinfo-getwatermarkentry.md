---
UID: NF:wmsdkidl.IWMWatermarkInfo.GetWatermarkEntry
title: IWMWatermarkInfo::GetWatermarkEntry (wmsdkidl.h)
description: The GetWatermarkEntry method retrieves information about one available watermarking system.
helpviewer_keywords: ["GetWatermarkEntry","GetWatermarkEntry method [windows Media Format]","GetWatermarkEntry method [windows Media Format]","IWMWatermarkInfo interface","IWMWatermarkInfo interface [windows Media Format]","GetWatermarkEntry method","IWMWatermarkInfo.GetWatermarkEntry","IWMWatermarkInfo::GetWatermarkEntry","IWMWatermarkInfoGetWatermarkEntry","wmformat.iwmwatermarkinfo_getwatermarkentry","wmsdkidl/IWMWatermarkInfo::GetWatermarkEntry"]
old-location: wmformat\iwmwatermarkinfo_getwatermarkentry.htm
tech.root: wmformat
ms.assetid: 7f303233-cd20-40ff-b564-4c44bf17a5f4
ms.date: 4/26/2023
ms.keywords: GetWatermarkEntry, GetWatermarkEntry method [windows Media Format], GetWatermarkEntry method [windows Media Format],IWMWatermarkInfo interface, IWMWatermarkInfo interface [windows Media Format],GetWatermarkEntry method, IWMWatermarkInfo.GetWatermarkEntry, IWMWatermarkInfo::GetWatermarkEntry, IWMWatermarkInfoGetWatermarkEntry, wmformat.iwmwatermarkinfo_getwatermarkentry, wmsdkidl/IWMWatermarkInfo::GetWatermarkEntry
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
 - IWMWatermarkInfo::GetWatermarkEntry
 - wmsdkidl/IWMWatermarkInfo::GetWatermarkEntry
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
 - IWMWatermarkInfo.GetWatermarkEntry
---

# IWMWatermarkInfo::GetWatermarkEntry


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetWatermarkEntry</b> method retrieves information about one available watermarking system.

## -parameters

### -param wmetType [in]

A value from the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_watermark_entry_type">WMT_WATERMARK_ENTRY_TYPE</a> enumeration type specifying the type of watermarking system.

### -param dwEntryNum [in]

<b>DWORD</b> containing the watermark entry number. This number is between zero and one less than the number of watermark entries returned by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwatermarkinfo-getwatermarkentrycount">IWMWatermarkInfo::GetWatermarkEntryCount</a>.

### -param pEntry [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_watermark_entry">WMT_WATERMARK_ENTRY</a> structure containing information about the specified watermarking system.

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
</table>

## -remarks

No watermarking <a href="/windows/desktop/wmformat/wmformat-glossary">DMOs</a> are provided with the Windows Media Format SDK. You can install third-party DMOs to use with your application.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo">IWMWatermarkInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwatermarkinfo-getwatermarkentrycount">IWMWatermarkInfo::GetWatermarkEntryCount</a>