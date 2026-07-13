---
UID: NF:wmsdkidl.IWMPacketSize.SetMaxPacketSize
title: IWMPacketSize::SetMaxPacketSize (wmsdkidl.h)
description: The SetMaxPacketSize method specifies the maximum size of a packet in an ASF file.
helpviewer_keywords: ["IWMPacketSize interface [windows Media Format]","SetMaxPacketSize method","IWMPacketSize.SetMaxPacketSize","IWMPacketSize2 interface [windows Media Format]","SetMaxPacketSize method","IWMPacketSize2::SetMaxPacketSize","IWMPacketSize::SetMaxPacketSize","IWMPacketSizeSetMaxPacketSize","SetMaxPacketSize","SetMaxPacketSize method [windows Media Format]","SetMaxPacketSize method [windows Media Format]","IWMPacketSize interface","SetMaxPacketSize method [windows Media Format]","IWMPacketSize2 interface","wmformat.iwmpacketsize_setmaxpacketsize","wmsdkidl/IWMPacketSize2::SetMaxPacketSize","wmsdkidl/IWMPacketSize::SetMaxPacketSize"]
old-location: wmformat\iwmpacketsize_setmaxpacketsize.htm
tech.root: wmformat
ms.assetid: a8230c08-e60f-454d-93a5-037685d6151c
ms.date: 4/26/2023
ms.keywords: IWMPacketSize interface [windows Media Format],SetMaxPacketSize method, IWMPacketSize.SetMaxPacketSize, IWMPacketSize2 interface [windows Media Format],SetMaxPacketSize method, IWMPacketSize2::SetMaxPacketSize, IWMPacketSize::SetMaxPacketSize, IWMPacketSizeSetMaxPacketSize, SetMaxPacketSize, SetMaxPacketSize method [windows Media Format], SetMaxPacketSize method [windows Media Format],IWMPacketSize interface, SetMaxPacketSize method [windows Media Format],IWMPacketSize2 interface, wmformat.iwmpacketsize_setmaxpacketsize, wmsdkidl/IWMPacketSize2::SetMaxPacketSize, wmsdkidl/IWMPacketSize::SetMaxPacketSize
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
 - IWMPacketSize::SetMaxPacketSize
 - wmsdkidl/IWMPacketSize::SetMaxPacketSize
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
 - IWMPacketSize.SetMaxPacketSize
 - IWMPacketSize2.SetMaxPacketSize
---

# IWMPacketSize::SetMaxPacketSize


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetMaxPacketSize</b> method specifies the maximum size of a <a href="/windows/desktop/wmformat/wmformat-glossary">packet</a> in an ASF file.

## -parameters

### -param dwMaxPacketSize [in]

<b>DWORD</b> containing the maximum packet size, in bytes. Set this to zero if the writer is to generate packets of various sizes. Otherwise, it must be a value between 100 bytes and 64 kilobytes.

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
The <i>dwMaxPacketSize</i> parameter contains an invalid value for the maximum packet size.

</td>
</tr>
</table>

## -remarks

By default, the maximum packet size is 1400 bytes (chosen because it is below the 1500-byte Ethernet maximum transition unit (MTU) plus the generic routing encapsulation (GRE) tunneling header size). The writer attempts to send 10 packets per second up to but not exceeding the value of the defined maximum packet size.

This method is designed for use with only single bit rate video; it should not be applied to a multiple bit rate stream. Note also that the maximum value applies only to the data; a small amount will be added for the header. For this reason there will be a small variance between the setting specified by this method and the actual maximum packet size reported by other tools for the stream.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2">IWMPacketSize2</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize-getmaxpacketsize">IWMPacketSize::GetMaxPacketSize</a>