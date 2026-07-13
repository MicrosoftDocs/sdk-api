---
UID: NF:wmsdkidl.IWMReaderPlaylistBurn.GetInitResults
title: IWMReaderPlaylistBurn::GetInitResults (wmsdkidl.h)
description: The GetInitResults method retrieves the results of the playlist file check.
helpviewer_keywords: ["GetInitResults","GetInitResults method [windows Media Format]","GetInitResults method [windows Media Format]","IWMReaderPlaylistBurn interface","IWMReaderPlaylistBurn interface [windows Media Format]","GetInitResults method","IWMReaderPlaylistBurn.GetInitResults","IWMReaderPlaylistBurn::GetInitResults","IWMReaderPlaylistBurnGetInitResults","wmformat.iwmreaderplaylistburn_getinitresults","wmsdkidl/IWMReaderPlaylistBurn::GetInitResults"]
old-location: wmformat\iwmreaderplaylistburn_getinitresults.htm
tech.root: wmformat
ms.assetid: 9f9db03b-0bcc-4442-b97e-f6a2f8d179fa
ms.date: 4/26/2023
ms.keywords: GetInitResults, GetInitResults method [windows Media Format], GetInitResults method [windows Media Format],IWMReaderPlaylistBurn interface, IWMReaderPlaylistBurn interface [windows Media Format],GetInitResults method, IWMReaderPlaylistBurn.GetInitResults, IWMReaderPlaylistBurn::GetInitResults, IWMReaderPlaylistBurnGetInitResults, wmformat.iwmreaderplaylistburn_getinitresults, wmsdkidl/IWMReaderPlaylistBurn::GetInitResults
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
 - IWMReaderPlaylistBurn::GetInitResults
 - wmsdkidl/IWMReaderPlaylistBurn::GetInitResults
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
 - IWMReaderPlaylistBurn.GetInitResults
---

# IWMReaderPlaylistBurn::GetInitResults


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetInitResults</b> method retrieves the results of the playlist file check.

## -parameters

### -param cFiles [in]

Number of files in the playlist. This is also the number of members in the array referenced by <i>phrStati</i>. This value must be the same as the number of files specified in the original call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn">InitPlaylistBurn</a>.

### -param phrStati [out]

Address of an array of <b>HRESULT</b> values. The members of this array correspond to the file names passed in the original call to <b>InitPlaylistBurn</b>. On output, each member is set to S_OK if the corresponding file is approved for copying as part of the playlist. If a file in the playlist is not licensed for copying, or if an error is encountered, the corresponding member of this array is set to the appropriate <b>HRESULT</b> return code.

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

This method should be called in response to a WMT_INIT_PLAYLIST_BURN message received by your implementation of the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> method. If you call <b>GetInitResults</b> without first calling <b>InitPlaylistBurn</b> and receiving the WMT_INIT_PLAYLIST_BURN message, <b>GetInitResults</b> will return an error code.

If, after calling this method, all members of the array referenced by <i>phrStati</i> are set to S_OK, you can begin copying the files in the playlist. However, you must use the same instance of the reader object for retrieving data that you used to get the <b>IWMReaderPlaylistBurn</b> interface.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn">IWMReaderPlaylistBurn Interface</a>