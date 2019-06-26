---
UID: NN:wuapi.IDownloadProgressChangedCallback
title: IDownloadProgressChangedCallback (wuapi.h)
author: windows-sdk-content
description: Handles the notification that indicates a change in the progress of an asynchronous download operation.
old-location: wua\idownloadprogresschangedcallback.htm
tech.root: Wua_Sdk
ms.assetid: 8fc414da-835c-438f-b607-8a273e7f9064
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDownloadProgressChangedCallback, IDownloadProgressChangedCallback interface [Windows Update Agent], IDownloadProgressChangedCallback interface [Windows Update Agent],described, wua.idownloadprogresschangedcallback, wuapi/IDownloadProgressChangedCallback
ms.topic: interface
f1_keywords: 
 - "wuapi/IDownloadProgressChangedCallback"
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
 - IDownloadProgressChangedCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDownloadProgressChangedCallback interface


## -description


Handles the notification that indicates a change in the progress of an asynchronous download operation.   This interface is implemented by programmers who call the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadProgressChangedCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDownloadProgressChangedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDownloadProgressChangedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogresschangedcallback-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of a change in the progress of an asynchronous download that was  initiated by calling <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a>.

</td>
</tr>
</table> 

