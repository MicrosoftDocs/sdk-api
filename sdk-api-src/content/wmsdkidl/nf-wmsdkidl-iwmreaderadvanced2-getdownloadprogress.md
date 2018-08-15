---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetDownloadProgress
title: IWMReaderAdvanced2::GetDownloadProgress
author: windows-sdk-content
description: The GetDownloadProgress method retrieves the percentage and amount of data that has been downloaded, and the time remaining to completion.
old-location: wmformat\iwmreaderadvanced2_getdownloadprogress.htm
old-project: wmformat
ms.assetid: 06bff83f-c3f2-4eca-85dd-7e7b93cfd73d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDownloadProgress, GetDownloadProgress method [windows Media Format], GetDownloadProgress method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetDownloadProgress method, IWMReaderAdvanced2.GetDownloadProgress, IWMReaderAdvanced2::GetDownloadProgress, IWMReaderAdvanced2GetDownloadProgress, wmformat.iwmreaderadvanced2_getdownloadprogress, wmsdkidl/IWMReaderAdvanced2::GetDownloadProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced2::GetDownloadProgress


## -description



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




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/da47fc9f-7762-4f92-8857-44a75a4cd00b">WMT_PLAY_MODE</a>
 

 

