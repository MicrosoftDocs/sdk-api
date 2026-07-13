---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetDownloadProgress
title: IWMReaderAdvanced2::GetDownloadProgress (wmsdkidl.h)
description: The GetDownloadProgress method retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.
helpviewer_keywords: ["GetDownloadProgress","GetDownloadProgress method [windows Media Format]","GetDownloadProgress method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetDownloadProgress method","IWMReaderAdvanced2.GetDownloadProgress","IWMReaderAdvanced2::GetDownloadProgress","IWMReaderAdvanced2GetDownloadProgress","wmformat.iwmreaderadvanced2_getdownloadprogress","wmsdkidl/IWMReaderAdvanced2::GetDownloadProgress"]
old-location: wmformat\iwmreaderadvanced2_getdownloadprogress.htm
tech.root: wmformat
ms.assetid: 06bff83f-c3f2-4eca-85dd-7e7b93cfd73d
ms.date: 4/26/2023
ms.keywords: GetDownloadProgress, GetDownloadProgress method [windows Media Format], GetDownloadProgress method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetDownloadProgress method, IWMReaderAdvanced2.GetDownloadProgress, IWMReaderAdvanced2::GetDownloadProgress, IWMReaderAdvanced2GetDownloadProgress, wmformat.iwmreaderadvanced2_getdownloadprogress, wmsdkidl/IWMReaderAdvanced2::GetDownloadProgress
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
 - IWMReaderAdvanced2::GetDownloadProgress
 - wmsdkidl/IWMReaderAdvanced2::GetDownloadProgress
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
 - IWMReaderAdvanced2.GetDownloadProgress
---

# IWMReaderAdvanced2::GetDownloadProgress


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDownloadProgress</b> method retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.

## -parameters

### -param pdwPercent [out]

Pointer to a <b>DWORD</b> containing the percentage of data that has been downloaded.

### -param pqwBytesDownloaded [out]

Pointer to a <b>QWORD</b> containing the number of bytes of data downloaded.

### -param pcnsDownload [out]

Pointer to variable specifying the time remaining, in 100-nanosecond units, for data to be downloaded.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be called to monitor progress while content is being downloaded from a Web server.

Content can be downloaded from a Web server when either the play mode is WMT_PLAY_MODE_AUDTOSELECT (in which case the reader automatically adjusts its play mode to DOWNLOAD) or the play mode is explicitly set to WMT_PLAY_MODE_DOWNLOAD.

If one of these two play modes is not current, and this method is called, all parameters return zero.

Before the first WMT_BUFFERING_START event, all the parameters return zero. Between WMT_BUFFERING_START and WMT_END_OF_STREAMING, the values for the percentage of downloading completed and number of bytes downloaded always increase. The value for the number of seconds of downloading remaining can go up or down depending on changing download rates. After WMT_END_OF_STREAMING has been sent, the percentage returns 100, bytes downloaded remains at the size of the download, and seconds remaining is zero.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_play_mode">WMT_PLAY_MODE</a>