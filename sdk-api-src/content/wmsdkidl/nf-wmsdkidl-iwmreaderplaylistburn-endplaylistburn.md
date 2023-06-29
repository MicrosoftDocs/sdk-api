---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.EndPlaylistBurn
title: IWMReaderPlaylistBurn::EndPlaylistBurn (wmsdkidl.h)
description: The EndPlaylistBurn method completes the playlist burn process. This includes releasing resources and adjusting counts associated with rights in DRM licenses.
helpviewer_keywords: ["EndPlaylistBurn","EndPlaylistBurn method [windows Media Format]","EndPlaylistBurn method [windows Media Format]","IWMReaderPlaylistBurn interface","IWMReaderPlaylistBurn interface [windows Media Format]","EndPlaylistBurn method","IWMReaderPlaylistBurn.EndPlaylistBurn","IWMReaderPlaylistBurn::EndPlaylistBurn","IWMReaderPlaylistBurnEndPlaylistBurn","wmformat.iwmreaderplaylistburn_endplaylistburn","wmsdkidl/IWMReaderPlaylistBurn::EndPlaylistBurn"]
old-location: wmformat\iwmreaderplaylistburn_endplaylistburn.htm
tech.root: wmformat
ms.assetid: 355f23eb-3cdb-4c27-bc48-499f349aef2b
ms.date: 4/26/2023
ms.keywords: EndPlaylistBurn, EndPlaylistBurn method [windows Media Format], EndPlaylistBurn method [windows Media Format],IWMReaderPlaylistBurn interface, IWMReaderPlaylistBurn interface [windows Media Format],EndPlaylistBurn method, IWMReaderPlaylistBurn.EndPlaylistBurn, IWMReaderPlaylistBurn::EndPlaylistBurn, IWMReaderPlaylistBurnEndPlaylistBurn, wmformat.iwmreaderplaylistburn_endplaylistburn, wmsdkidl/IWMReaderPlaylistBurn::EndPlaylistBurn
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMReaderPlaylistBurn::EndPlaylistBurn
 - wmsdkidl/IWMReaderPlaylistBurn::EndPlaylistBurn
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
 - IWMReaderPlaylistBurn.EndPlaylistBurn
---

# IWMReaderPlaylistBurn::EndPlaylistBurn


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>EndPlaylistBurn</b> method completes the playlist burn process. This includes releasing resources and adjusting counts associated with rights in DRM licenses.

## -parameters

### -param hrBurnResult [in]

Result of the playlist burn. Set to S_OK if the files in the playlist were successfully copied to CD. Otherwise, set to an appropriate <b>HRESULT</b> error code.

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

To abort the playlist burn process after your status callback receives the WMT_INIT_PLAYLIST_BURN message, pass the E_ABORT error code. To stop the process before initialization is complete, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-cancel">Cancel</a> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn">IWMReaderPlaylistBurn Interface</a>