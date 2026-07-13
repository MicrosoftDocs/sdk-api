---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetClientInfo
title: IWMReaderAdvanced::SetClientInfo (wmsdkidl.h)
description: The SetClientInfo method sets client-side information used for logging.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetClientInfo method","IWMReaderAdvanced.SetClientInfo","IWMReaderAdvanced::SetClientInfo","IWMReaderAdvancedSetClientInfo","SetClientInfo","SetClientInfo method [windows Media Format]","SetClientInfo method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setclientinfo","wmsdkidl/IWMReaderAdvanced::SetClientInfo"]
old-location: wmformat\iwmreaderadvanced_setclientinfo.htm
tech.root: wmformat
ms.assetid: dec93690-8285-4672-bf70-63f3c10294bf
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetClientInfo method, IWMReaderAdvanced.SetClientInfo, IWMReaderAdvanced::SetClientInfo, IWMReaderAdvancedSetClientInfo, SetClientInfo, SetClientInfo method [windows Media Format], SetClientInfo method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setclientinfo, wmsdkidl/IWMReaderAdvanced::SetClientInfo
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
 - IWMReaderAdvanced::SetClientInfo
 - wmsdkidl/IWMReaderAdvanced::SetClientInfo
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
 - IWMReaderAdvanced.SetClientInfo
---

# IWMReaderAdvanced::SetClientInfo


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetClientInfo</b> method sets client-side information used for logging. Use this method to specify information about the client that the reader object sends to the server for logging. If the application does not call this method, the reader object uses default values.

## -parameters

### -param pClientInfo [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo">WM_READER_CLIENTINFO</a> structure allocated by the caller, which contains information about the client.

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
Invalid argument. The <b>cbSize</b> member must be set, and the string values must not exceed 1024 characters.

</td>
</tr>
</table>

## -remarks

Initialize the <b>WM_READER_CLIENTINFO</b> structure before calling this method. Always set the <b>cbSize</b> member equal to the size of the structure, and set any unused fields to zero.


```cpp

WM_READER_CLIENTINFO info;
ZeroMemory(&info, sizeof(WM_READER_CLIENTINFO));
info.cbSize = sizeof(WM_READER_CLIENTINFO);

// Set other fields (not shown).

hr = pReaderAdvanced->SetClientInfo( &info );

```

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>