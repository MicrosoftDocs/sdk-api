---
UID: NN:wuapi.IDownloadJob
title: IDownloadJob
author: windows-driver-content
description: Contains properties and methods that are available to a download operation.
old-location: wua\idownloadjob.htm
old-project: Wua_Sdk
ms.assetid: 0157acab-53b6-43f9-a358-81cd5108c531
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IDownloadJob, IDownloadJob interface [Windows Update Agent], IDownloadJob interface [Windows Update Agent], described, wua.idownloadjob, wuapi/IDownloadJob
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IDownloadJob
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IDownloadJob interface


## -description


Contains properties and methods that are available to a download operation.  This interface is returned by the   <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadJob</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDownloadJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0910acbc-81d7-44ae-bae1-26c82b33d29b">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to be completed and releases all callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e87c85cf-0011-4edb-a409-0b4db3292caf">GetProgress</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface that describes the current progress of a download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01f403c5-b73d-4366-8e9e-132f373a354f">RequestAbort</a>
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

<a href="https://msdn.microsoft.com/47d2af4a-c04f-4413-ad29-3b8cb1292539">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets  the caller-specific state object that is passed to the <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d63f1bfc-589c-4cd2-95dd-e8c88e7f593c">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets  the setting that indicates whether the call to <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> was processed completely.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43ceffc8-f045-4cac-976a-2357ab0d1283">Updates</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains a read-only collection of the updates that are specified in a download.

</td>
</tr>
</table> 

