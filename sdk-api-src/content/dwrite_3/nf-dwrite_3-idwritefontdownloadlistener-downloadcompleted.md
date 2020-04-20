---
UID: NF:dwrite_3.IDWriteFontDownloadListener.DownloadCompleted
title: IDWriteFontDownloadListener::DownloadCompleted (dwrite_3.h)
description: The DownloadCompleted method is called back on an arbitrary thread when a download operation ends.helpviewer_keywords: ["DownloadCompleted","DownloadCompleted method [Direct Write]","DownloadCompleted method [Direct Write]","IDWriteFontDownloadListener interface","IDWriteFontDownloadListener interface [Direct Write]","DownloadCompleted method","IDWriteFontDownloadListener.DownloadCompleted","IDWriteFontDownloadListener::DownloadCompleted","directwrite.idwritefontdownloadlistener_downloadcompleted","dwrite_3/IDWriteFontDownloadListener::DownloadCompleted"]
old-location: directwrite\idwritefontdownloadlistener_downloadcompleted.htm
tech.root: DirectWrite
ms.assetid: d4da0189-efe4-4ee6-4cc9-179fbda54b98
ms.date: 12/05/2018
ms.keywords: DownloadCompleted, DownloadCompleted method [Direct Write], DownloadCompleted method [Direct Write],IDWriteFontDownloadListener interface, IDWriteFontDownloadListener interface [Direct Write],DownloadCompleted method, IDWriteFontDownloadListener.DownloadCompleted, IDWriteFontDownloadListener::DownloadCompleted, directwrite.idwritefontdownloadlistener_downloadcompleted, dwrite_3/IDWriteFontDownloadListener::DownloadCompleted
f1_keywords:
- dwrite_3/IDWriteFontDownloadListener.DownloadCompleted
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontDownloadListener::DownloadCompleted


## -description


The DownloadCompleted method is called back on an arbitrary thread when a    
    download operation ends. 


## -parameters




### -param downloadQueue [in]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>*</b>

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


## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener">IDWriteFontDownloadListener</a>
 

 

