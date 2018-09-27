---
UID: NN:wuapi.IDownloadCompletedCallback
title: IDownloadCompletedCallback
author: windows-sdk-content
description: Provides the callback that is used when an asynchronous download is completed.
old-location: wua\idownloadcompletedcallback.htm
tech.root: wua_sdk
ms.assetid: ad1c3075-21d9-409f-9677-fbf6d0c50313
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IDownloadCompletedCallback, IDownloadCompletedCallback interface [Windows Update Agent], IDownloadCompletedCallback interface [Windows Update Agent],described, wua.idownloadcompletedcallback, wuapi/IDownloadCompletedCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IDownloadCompletedCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadCompletedCallback interface


## -description


Provides the callback that is used when an asynchronous download is completed.   This interface is implemented by programmers who call the <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader::BeginDownload</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadCompletedCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDownloadCompletedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDownloadCompletedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87334ff3-bfb0-48cb-b2e1-ea6d4617638d">Invoke</a>
</td>
<td align="left" width="63%">
Notifies the caller that the download is complete.

</td>
</tr>
</table> 

