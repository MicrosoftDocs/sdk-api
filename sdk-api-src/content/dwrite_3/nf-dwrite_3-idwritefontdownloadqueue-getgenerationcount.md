---
UID: NF:dwrite_3.IDWriteFontDownloadQueue.GetGenerationCount
title: IDWriteFontDownloadQueue::GetGenerationCount
author: windows-sdk-content
description: Gets the current generation number of the download queue, which is incremented every time after a download completes, whether failed or successful. This cookie value can be compared against cached data to determine if it is stale.
old-location: directwrite\idwritefontdownloadqueue_getgenerationcount.htm
tech.root: DirectWrite
ms.assetid: 6fbbe575-b186-7ffb-ff32-efceccccc48c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetGenerationCount, GetGenerationCount method [Direct Write], GetGenerationCount method [Direct Write],IDWriteFontDownloadQueue interface, IDWriteFontDownloadQueue interface [Direct Write],GetGenerationCount method, IDWriteFontDownloadQueue.GetGenerationCount, IDWriteFontDownloadQueue::GetGenerationCount, directwrite.idwritefontdownloadqueue_getgenerationcount, dwrite_3/IDWriteFontDownloadQueue::GetGenerationCount
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
 - IDWriteFontDownloadQueue.GetGenerationCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontDownloadQueue::GetGenerationCount


## -description


Gets the current generation number of the download queue, which is incremented   
    every time after a download completes, whether failed or successful. This cookie  
    value can be compared against cached data to determine if it is stale.


## -parameters






## -returns



Type: <b>UINT64</b>

The current generation number of the download queue.




## -see-also




<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>
 

 

