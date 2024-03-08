---
UID: NF:wmsdkidl.IWMProfile3.GetExpectedPacketCount
title: IWMProfile3::GetExpectedPacketCount (wmsdkidl.h)
description: The GetExpectedPacketCount method calculates the expected packet count for the specified duration. The packet count returned is only an estimate, and it is based upon the settings of the profile at the time this call is made.
helpviewer_keywords: ["GetExpectedPacketCount","GetExpectedPacketCount method [windows Media Format]","GetExpectedPacketCount method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetExpectedPacketCount method","IWMProfile3.GetExpectedPacketCount","IWMProfile3::GetExpectedPacketCount","IWMProfile3GetExpectedPacketCount","wmformat.iwmprofile3_getexpectedpacketcount","wmsdkidl/IWMProfile3::GetExpectedPacketCount"]
old-location: wmformat\iwmprofile3_getexpectedpacketcount.htm
tech.root: wmformat
ms.assetid: ddab3735-06a1-4e03-9abc-0fca635ef759
ms.date: 4/26/2023
ms.keywords: GetExpectedPacketCount, GetExpectedPacketCount method [windows Media Format], GetExpectedPacketCount method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetExpectedPacketCount method, IWMProfile3.GetExpectedPacketCount, IWMProfile3::GetExpectedPacketCount, IWMProfile3GetExpectedPacketCount, wmformat.iwmprofile3_getexpectedpacketcount, wmsdkidl/IWMProfile3::GetExpectedPacketCount
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
 - IWMProfile3::GetExpectedPacketCount
 - wmsdkidl/IWMProfile3::GetExpectedPacketCount
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
 - IWMProfile3.GetExpectedPacketCount
---

# IWMProfile3::GetExpectedPacketCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetExpectedPacketCount</b> method calculates the expected <a href="/windows/desktop/wmformat/wmformat-glossary">packet</a> count for the specified duration. The packet count returned is only an estimate, and it is based upon the settings of the profile at the time this call is made.

## -parameters

### -param msDuration [in]

Specifies the duration in milliseconds.

### -param pcPackets [out]

Pointer to receive the count of packets expected for <i>msDuration</i> milliseconds.

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
<i>pcPackets</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
One of the internal objects required by the method could not be initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The profile in the profile object is not compatible with this method.

</td>
</tr>
</table>

## -remarks

Problems will arise if the value passed in <i>msDuration</i> is not a positive number of milliseconds. The method will return S_OK as normal, but the packet count returned will not be correct.

It is impossible for this method to give exact counts, because there is no way to account for interleaved data in an encoded file. The packet count returned is most accurate for files with one audio stream. The more complicated the profile, the less accurate the packet count will be.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>