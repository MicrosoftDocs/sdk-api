---
UID: NN:wuapi.IDownloadJob
title: IDownloadJob (wuapi.h)
description: Contains properties and methods that are available to a download operation.
helpviewer_keywords: ["IDownloadJob","IDownloadJob interface [Windows Update Agent]","IDownloadJob interface [Windows Update Agent]","described","wua.idownloadjob","wuapi/IDownloadJob"]
old-location: wua\idownloadjob.htm
tech.root: wua
ms.assetid: 0157acab-53b6-43f9-a358-81cd5108c531
ms.date: 12/05/2018
ms.keywords: IDownloadJob, IDownloadJob interface [Windows Update Agent], IDownloadJob interface [Windows Update Agent],described, wua.idownloadjob, wuapi/IDownloadJob
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDownloadJob
 - wuapi/IDownloadJob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IDownloadJob
---

# IDownloadJob interface


## -description

Contains properties and methods that are available to a download operation.  This interface is returned by the   <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadJob</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDownloadJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDownloadJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-cleanup">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to be completed and releases all callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a> interface that describes the current progress of a download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-requestabort">RequestAbort</a>
</td>
<td align="left" width="63%">
Makes a request to end an asynchronous download.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-get_asyncstate">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets  the caller-specific state object that is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-get_iscompleted">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets  the setting that indicates whether the call to <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> was processed completely.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadjob-get_updates">Updates</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains a read-only collection of the updates that are specified in a download.

</td>
</tr>
</table>

