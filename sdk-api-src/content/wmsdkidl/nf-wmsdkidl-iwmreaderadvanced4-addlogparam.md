---
UID: NF:wmsdkidl.IWMReaderAdvanced4.AddLogParam
title: IWMReaderAdvanced4::AddLogParam (wmsdkidl.h)
description: The AddLogParam method adds a named value to the logging information that the reader object will send to the sever.
helpviewer_keywords: ["AddLogParam","AddLogParam method [windows Media Format]","AddLogParam method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","AddLogParam method","IWMReaderAdvanced4.AddLogParam","IWMReaderAdvanced4::AddLogParam","IWMReaderAdvanced4AddLogParam","wmformat.iwmreaderadvanced4_addlogparam","wmsdkidl/IWMReaderAdvanced4::AddLogParam"]
old-location: wmformat\iwmreaderadvanced4_addlogparam.htm
tech.root: wmformat
ms.assetid: 7d117895-b61f-4890-8cb6-3e4ecf49ca99
ms.date: 4/26/2023
ms.keywords: AddLogParam, AddLogParam method [windows Media Format], AddLogParam method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],AddLogParam method, IWMReaderAdvanced4.AddLogParam, IWMReaderAdvanced4::AddLogParam, IWMReaderAdvanced4AddLogParam, wmformat.iwmreaderadvanced4_addlogparam, wmsdkidl/IWMReaderAdvanced4::AddLogParam
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
 - IWMReaderAdvanced4::AddLogParam
 - wmsdkidl/IWMReaderAdvanced4::AddLogParam
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
 - IWMReaderAdvanced4.AddLogParam
---

# IWMReaderAdvanced4::AddLogParam


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddLogParam</b> method adds a named value to the logging information that the reader object will send to the sever.

## -parameters

### -param wszNameSpace [in]

Optional wide-character string that contains the namespace for the log entry. This parameter can be <b>NULL</b>. Namespace names are limited to 1024 wide characters.

### -param wszName [in]

Wide-character string that contains the name of the log entry. Log entry names are limited to 1024 wide characters.

### -param wszValue [in]

Wide-character string that contains the value of the log entry. Log entry values are limited to 1024 wide characters.

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
One of the parameters exceeded the allowed string length.

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
</table>

## -remarks

The reader object sends logging data to the server in the form of an XML stream. The <b>AddLogParam</b> method enables the client to specify additional logging entries. The <i>wszNameSpace</i> parameter can be used to specify an XML namespace for the new entry. If you do not specify a namespace, the default namespace is used. However, the reader will not override log entries already defined by the server, with the following exception: If the server specifies an empty string ("") for the cs-media-role or cs-media-name entry, you can overwrite these entries. By default, a server running Windows Media Services 9 Series sends an empty string for cs-media-role, and the name of the file for cs-media-name.

To send the logging information to the server, call the <b>SendLogParams</b> method. To retrieve the log entries on the server, you must provide a custom logging plug-in, using the Windows Media Services 9 Series SDK. The default logging plug-in writes just the W3C-compliant log summary, so custom log entries are not included in the log.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-sendlogparams">IWMReaderAdvanced4::SendLogParams</a>