---
UID: NF:wmsdkidl.IWMProfile3.GetBandwidthSharingCount
title: IWMProfile3::GetBandwidthSharingCount (wmsdkidl.h)
description: The GetBandwidthSharingCount method retrieves the total number of bandwidth sharing objects that have been added to the profile.
helpviewer_keywords: ["GetBandwidthSharingCount","GetBandwidthSharingCount method [windows Media Format]","GetBandwidthSharingCount method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetBandwidthSharingCount method","IWMProfile3.GetBandwidthSharingCount","IWMProfile3::GetBandwidthSharingCount","IWMProfile3GetBandwidthSharingCount","wmformat.iwmprofile3_getbandwidthsharingcount","wmsdkidl/IWMProfile3::GetBandwidthSharingCount"]
old-location: wmformat\iwmprofile3_getbandwidthsharingcount.htm
tech.root: wmformat
ms.assetid: 7f5a11a7-d81a-4ca1-8b0f-1d561f736523
ms.date: 4/26/2023
ms.keywords: GetBandwidthSharingCount, GetBandwidthSharingCount method [windows Media Format], GetBandwidthSharingCount method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetBandwidthSharingCount method, IWMProfile3.GetBandwidthSharingCount, IWMProfile3::GetBandwidthSharingCount, IWMProfile3GetBandwidthSharingCount, wmformat.iwmprofile3_getbandwidthsharingcount, wmsdkidl/IWMProfile3::GetBandwidthSharingCount
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
 - IWMProfile3::GetBandwidthSharingCount
 - wmsdkidl/IWMProfile3::GetBandwidthSharingCount
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
 - IWMProfile3.GetBandwidthSharingCount
---

# IWMProfile3::GetBandwidthSharingCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetBandwidthSharingCount</b> method retrieves the total number of bandwidth sharing objects that have been added to the profile.

## -parameters

### -param pcBS [out]

Pointer to receive the total number of bandwidth sharing objects.

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
<i>pcBS</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">IWMProfile3::GetBandwidthSharing</a>