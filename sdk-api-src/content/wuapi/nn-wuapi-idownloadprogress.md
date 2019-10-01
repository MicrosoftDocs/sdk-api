---
UID: NN:wuapi.IDownloadProgress
title: IDownloadProgress (wuapi.h)
author: windows-sdk-content
description: Represents the progress of an asynchronous download operation.
old-location: wua\idownloadprogress.htm
tech.root: Wua_Sdk
ms.assetid: 773de760-5fde-4975-ba8d-d20b3affb4a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDownloadProgress, IDownloadProgress interface [Windows Update Agent], IDownloadProgress interface [Windows Update Agent],described, wua.idownloadprogress, wuapi/IDownloadProgress
ms.topic: interface
f1_keywords: 
 - "wuapi/IDownloadProgress"
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
 - IDownloadProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDownloadProgress interface


## -description


Represents the progress of an asynchronous download operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadProgress</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDownloadProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDownloadProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-getupdateresult">GetUpdateResult</a>
</td>
<td align="left" width="63%">
Returns the result of the download of a specified update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadProgress</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded">CurrentUpdateBytesDownloaded</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload">CurrentUpdateBytesToDownload</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase">CurrentUpdateDownloadPhase</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/ne-wuapi-downloadphase">DownloadPhase</a> enumeration value that specifies the phase of the download that is currently in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/aa385880(v=vs.85)">CurrentUpdateIndex</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete">CurrentUpdatePercentComplete</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an estimate of the percentage of the current update that has been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_percentcomplete">PercentComplete</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an estimate of the percentage of all the updates that have been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded">TotalBytesDownloaded</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a string that specifies the total amount of data that has been downloaded, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload">TotalBytesToDownload</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.

</td>
</tr>
</table> 

