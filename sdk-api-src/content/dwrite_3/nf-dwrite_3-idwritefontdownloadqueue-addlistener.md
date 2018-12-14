---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.AddListener
title: IDWriteFontDownloadQueue::AddListener
author: windows-sdk-content
description: Registers a client-defined listener object that receives download notifications. All registered listener's DownloadCompleted will be called after BeginDownloadcompletes.
old-location: directwrite\idwritefontdownloadqueue_addlistener.htm
tech.root: DirectWrite
ms.assetid: c539be2d-bc77-cc8a-c78c-226a67b8dd26
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddListener, AddListener method [Direct Write], AddListener method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],AddListener method, IDWriteFontDownloadQueue.AddListener, IDWriteFontDownloadQueue::AddListener, directwrite.idwritefontdownloadqueue_addlistener, dwrite_3/IDWriteFontDownloadQueue::AddListener
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
 - IDWriteFontDownloadQueue.AddListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontDownloadQueue::AddListener


## -description


Registers a client-defined listener object that receives download notifications.  
    All registered listener's DownloadCompleted will be called after <a href="https://msdn.microsoft.com/en-us/library/Dn894554(v=VS.85).aspx">BeginDownload</a>completes. 


## -parameters




### -param listener

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn890775(v=VS.85).aspx">IDWriteFontDownloadListener</a>*</b>

Listener object to add.


### -param token [out]

Type: <b>UINT32*</b>

Receives a token value, which the caller must subsequently pass to <a href="https://msdn.microsoft.com/en-us/library/Dn894559(v=VS.85).aspx">RemoveListener</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/Dn890775(v=VS.85).aspx">IDWriteFontDownloadListener</a> can also be passed to <a href="https://msdn.microsoft.com/en-us/library/Dn894554(v=VS.85).aspx">BeginDownload</a> 
      using the context parameter, rather than globally registered to the queue.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn890778(v=VS.85).aspx">IDWriteFontDownloadQueue</a>
 

 

