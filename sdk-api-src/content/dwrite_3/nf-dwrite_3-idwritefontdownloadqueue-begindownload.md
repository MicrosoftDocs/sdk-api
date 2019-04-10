---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.BeginDownload
title: IDWriteFontDownloadQueue::BeginDownload (dwrite_3.h)
author: windows-sdk-content
description: Begins an asynchronous download operation. The download operation executes in the background until it completes or is cancelled by a CancelDownload call.
old-location: directwrite\idwritefontdownloadqueue_begindownload.htm
tech.root: DirectWrite
ms.assetid: 1e3b200c-0190-f600-1cb6-4e2a46f882b4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginDownload, BeginDownload method [Direct Write], BeginDownload method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],BeginDownload method, IDWriteFontDownloadQueue.BeginDownload, IDWriteFontDownloadQueue::BeginDownload, directwrite.idwritefontdownloadqueue_begindownload, dwrite_3/IDWriteFontDownloadQueue::BeginDownload
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontDownloadQueue.BeginDownload
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontDownloadQueue::BeginDownload


## -description


Begins an asynchronous download operation. The download operation executes   
    in the background until it completes or is cancelled by a <a href="https://msdn.microsoft.com/f2ecabcf-3301-d446-8eda-4536b3f9b5e3">CancelDownload</a> call.


## -parameters




### -param context [in, optional]

Type: <b>IUnknown*</b>

Optional context object that is passed back to the     
          download notification handler's DownloadCompleted method. If the context object  
          implements IDWriteFontDownloadListener, its DownloadCompleted will be called    
          when done.


## -returns



Type: <b>HRESULT</b>

 Returns S_OK if a download was successfully begun, S_FALSE if the queue was 
          empty, or a standard HRESULT error code.




## -remarks



BeginDownload removes all download requests from the queue, transferring them   
      to a background download operation. If any previous downloads are still ongoing     
      when BeginDownload is called again, the new download does not complete until     
      the previous downloads have finished. 




## -see-also




<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>
 

 

