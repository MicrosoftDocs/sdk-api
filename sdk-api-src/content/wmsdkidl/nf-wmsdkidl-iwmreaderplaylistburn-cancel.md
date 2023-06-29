---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.Cancel
title: IWMReaderPlaylistBurn::Cancel (wmsdkidl.h)
description: The Cancel method cancels an initiated playlist burn before initialization is finished.
helpviewer_keywords: ["Cancel","Cancel method [windows Media Format]","Cancel method [windows Media Format]","IWMReaderPlaylistBurn interface","IWMReaderPlaylistBurn interface [windows Media Format]","Cancel method","IWMReaderPlaylistBurn.Cancel","IWMReaderPlaylistBurn::Cancel","IWMReaderPlaylistBurnCancel","wmformat.iwmreaderplaylistburn_cancel","wmsdkidl/IWMReaderPlaylistBurn::Cancel"]
old-location: wmformat\iwmreaderplaylistburn_cancel.htm
tech.root: wmformat
ms.assetid: d126f13b-90ac-489e-8dd0-e507f4003a7a
ms.date: 4/26/2023
ms.keywords: Cancel, Cancel method [windows Media Format], Cancel method [windows Media Format],IWMReaderPlaylistBurn interface, IWMReaderPlaylistBurn interface [windows Media Format],Cancel method, IWMReaderPlaylistBurn.Cancel, IWMReaderPlaylistBurn::Cancel, IWMReaderPlaylistBurnCancel, wmformat.iwmreaderplaylistburn_cancel, wmsdkidl/IWMReaderPlaylistBurn::Cancel
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
 - IWMReaderPlaylistBurn::Cancel
 - wmsdkidl/IWMReaderPlaylistBurn::Cancel
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
 - IWMReaderPlaylistBurn.Cancel
---

# IWMReaderPlaylistBurn::Cancel


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Cancel</b> method cancels an initiated playlist burn before initialization is finished.



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

You should call this method to cancel the playlist burn process only after calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn">InitPlaylistBurn</a> and before your status callback receives the WMT_INIT_PLAYLIST_BURN message. If you need to cancel the playlist burn after initialization is finished, you should call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn">EndPlaylistBurn</a> method and pass the E_ABORT error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn">IWMReaderPlaylistBurn Interface</a>
