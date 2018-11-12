---
UID: NF:dwrite_3.IDWriteFontDownloadListener.DownloadCompleted
title: IDWriteFontDownloadListener::DownloadCompleted
author: windows-sdk-content
description: The DownloadCompleted method is called back on an arbitrary thread when a download operation ends.
old-location: directwrite\idwritefontdownloadlistener_downloadcompleted.htm
tech.root: DirectWrite
ms.assetid: d4da0189-efe4-4ee6-4cc9-179fbda54b98
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DownloadCompleted, DownloadCompleted method [Direct Write], DownloadCompleted method [Direct Write],IDWriteFontDownloadListener interface, IDWriteFontDownloadListener interface [Direct Write],DownloadCompleted method, IDWriteFontDownloadListener.DownloadCompleted, IDWriteFontDownloadListener::DownloadCompleted, directwrite.idwritefontdownloadlistener_downloadcompleted, dwrite_3/IDWriteFontDownloadListener::DownloadCompleted
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDWriteFontDownloadListener.DownloadCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontDownloadListener::DownloadCompleted


## -description


The DownloadCompleted method is called back on an arbitrary thread when a    
    download operation ends. 


## -parameters




### -param downloadQueue [in]

Type: <b><a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>*</b>

Pointer to the download queue interface on which     
          the BeginDownload method was called.


### -param context [in, optional]

Type: <b>IUnknown*</b>

Optional context object that was passed to BeginDownload.    
          AddRef is called on the context object by BeginDownload and Release is called  
          after the DownloadCompleted method returns.


### -param downloadResult

Type: <b>HRESULT</b>

Result of the download operation.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/92678d34-9a14-8d58-129c-be31a0963942">IDWriteFontDownloadListener</a>
 

 

