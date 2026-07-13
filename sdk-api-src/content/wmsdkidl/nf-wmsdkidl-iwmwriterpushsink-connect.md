---
UID: NF:wmsdkidl.IWMWriterPushSink.Connect
title: IWMWriterPushSink::Connect (wmsdkidl.h)
description: The Connect method connects to a publishing point on a Windows Media server.
helpviewer_keywords: ["Connect","Connect method [windows Media Format]","Connect method [windows Media Format]","IWMWriterPushSink interface","IWMWriterPushSink interface [windows Media Format]","Connect method","IWMWriterPushSink.Connect","IWMWriterPushSink::Connect","IWMWriterPushSinkConnect","wmformat.iwmwriterpushsink_connect","wmsdkidl/IWMWriterPushSink::Connect"]
old-location: wmformat\iwmwriterpushsink_connect.htm
tech.root: wmformat
ms.assetid: 5934697e-5d7c-4681-a424-9ad764dfeab1
ms.date: 4/26/2023
ms.keywords: Connect, Connect method [windows Media Format], Connect method [windows Media Format],IWMWriterPushSink interface, IWMWriterPushSink interface [windows Media Format],Connect method, IWMWriterPushSink.Connect, IWMWriterPushSink::Connect, IWMWriterPushSinkConnect, wmformat.iwmwriterpushsink_connect, wmsdkidl/IWMWriterPushSink::Connect
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
 - IWMWriterPushSink::Connect
 - wmsdkidl/IWMWriterPushSink::Connect
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
 - IWMWriterPushSink.Connect
---

# IWMWriterPushSink::Connect


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Connect</b> method connects to a publishing point on a Windows Media server.

## -parameters

### -param pwszURL [in]

Wide-character string that contains the URL of the publishing point on the Windows Media server. For example, if the URL is "http://MyServer/MyPublishingPoint", the push sink connects to the publishing point named MyPublishingPoint on the server named MyServer. The default port number is 80. If the server is using a different port, specify the port number in the URL. For example, "http://MyServer:8080/MyPublishingPoint" specifies port number 8080.

### -param pwszTemplateURL [in]

Optional wide-character string that contains the URL of an existing publishing point to use as a template. This parameter can be <b>NULL</b>.

### -param fAutoDestroy [in]

Boolean value that specifies whether to remove the publishing point after the push sink disconnects from the server.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>pwszURL</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
Host name is not valid.

</td>
</tr>
</table>

## -remarks

If the publishing point specified in <i>pwsURL</i> does not exist, the server creates a new publishing point. The caller must have write and create permissions on the server. The new publishing point has the same configuration as the publishing point specified in the <i>pwszTemplateURL</i> parameter. If <i>pwszTemplateURL</i> is <b>NULL</b>, the new publishing point has the same configuration as the server's default publishing point.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink">IWMWriterPushSink Interface</a>