---
UID: NF:wmsdkidl.IWMReader.Open
title: IWMReader::Open (wmsdkidl.h)
description: The Open method opens an ASF file for reading.
helpviewer_keywords: ["IWMReader interface [windows Media Format]","Open method","IWMReader.Open","IWMReader::Open","IWMReaderOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMReader interface","wmformat.iwmreader_open","wmsdkidl/IWMReader::Open"]
old-location: wmformat\iwmreader_open.htm
tech.root: wmformat
ms.assetid: ab5b7f9e-b647-4121-abb3-2c9deb1f50cc
ms.date: 4/26/2023
ms.keywords: IWMReader interface [windows Media Format],Open method, IWMReader.Open, IWMReader::Open, IWMReaderOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMReader interface, wmformat.iwmreader_open, wmsdkidl/IWMReader::Open
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
 - IWMReader::Open
 - wmsdkidl/IWMReader::Open
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
 - IWMReader.Open
---

# IWMReader::Open


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Open</b> method opens an ASF file for reading.

## -parameters

### -param pwszURL [in]

Pointer to a wide-character <b>null</b>-terminated string containing the path and name of the file to be opened. This method accepts a path to a folder on a local machine, a path to a network share, or a uniform resource locator (URL).

### -param pCallback [in]

Pointer to the object that implements the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback</a> interface.

### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to <b>OnStatus</b>.

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
The <i>pCallback</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

This method is asynchronous; it returns very quickly and sends a WMT_OPENED status notification to the application's <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method when the file is opened and ready for use.

Because the method returns before the file is opened, a return value of S_OK does not necessarily mean that the file has been opened successfully. To ascertain the success of the call, you must check the value of the <i>hr</i> parameter of <b>OnStatus</b> when the WMT_OPENED notification is received.

If <i>hr</i> equals NS_E_NO_STREAM it means that the header is not yet available, and that a WMT_SOURCE_SWITCH event will be sent as soon as the header becomes available. No WMT_EOF will be sent before the WMT_SOURCE_SWITCH.

Applications that read files from behind a firewall will have better performance when opening files if the address is specified using the domain name server (DNS) name instead of the IP address.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-close">IWMReader::Close</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-stop">IWMReader::Stop</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream">IWMReaderAdvanced2::OpenStream</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a>