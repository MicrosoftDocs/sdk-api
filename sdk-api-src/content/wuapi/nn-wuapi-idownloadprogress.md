---
UID: NN:wuapi.IDownloadProgress
title: IDownloadProgress
author: windows-sdk-content
description: Represents the progress of an asynchronous download operation.
old-location: wua\idownloadprogress.htm
tech.root: wua_sdk
ms.assetid: 773de760-5fde-4975-ba8d-d20b3affb4a7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDownloadProgress, IDownloadProgress interface [Windows Update Agent], IDownloadProgress interface [Windows Update Agent],described, wua.idownloadprogress, wuapi/IDownloadProgress
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
 - IDownloadProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadProgress interface


## -description


Represents the progress of an asynchronous download operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadProgress</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDownloadProgress</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e7474a0a-98dc-4dd6-b5b8-8f88f0539f9a">GetUpdateResult</a>
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

<a href="https://msdn.microsoft.com/48ba3ab9-405d-474b-a85b-fe70db343433">CurrentUpdateBytesDownloaded</a>


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

<a href="https://msdn.microsoft.com/6e3ac04f-b827-4369-981e-af7a437f5e5c">CurrentUpdateBytesToDownload</a>


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

<a href="https://msdn.microsoft.com/5c94b0e9-c137-4677-a014-b8467a8049e5">CurrentUpdateDownloadPhase</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a <a href="https://msdn.microsoft.com/a7e930dd-1dfa-42cc-9761-d4252c9a92ae">DownloadPhase</a> enumeration value that specifies the phase of the download that is currently in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e357229d-cfb3-4ed6-b5b4-2e830fbda1ba">CurrentUpdateIndex</a>


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

<a href="https://msdn.microsoft.com/7dad425f-721a-4c4a-938b-d4de51f38dee">CurrentUpdatePercentComplete</a>


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

<a href="https://msdn.microsoft.com/af6a4424-eaf4-438b-b879-a9f3da3044ca">PercentComplete</a>


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

<a href="https://msdn.microsoft.com/83d8f7d2-e06d-461a-be45-ebbb448b2480">TotalBytesDownloaded</a>


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

<a href="https://msdn.microsoft.com/607e1d18-1df3-40c1-9104-de902561ede0">TotalBytesToDownload</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.

</td>
</tr>
</table> 

