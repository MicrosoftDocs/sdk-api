---
UID: NN:wuapi.IDownloadResult
title: IDownloadResult
author: windows-sdk-content
description: Represents the result of a download operation.
old-location: wua\idownloadresult.htm
old-project: Wua_Sdk
ms.assetid: 293bea59-acec-4774-adb9-1ad1d29406c3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDownloadResult, IDownloadResult interface [Windows Update Agent], IDownloadResult interface [Windows Update Agent],described, wua.idownloadresult, wuapi/IDownloadResult
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
tech.root: 
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IDownloadResult
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IDownloadResult interface


## -description


The <b>IDownloadResult</b> interface represents the result of a download operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadResult</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDownloadResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDownloadResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d95ce8ad-74d7-4144-9a4b-75d69d5a9442">GetUpdateResult</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/d2a800c9-c23a-4aab-a9c6-e408349818dd">IUpdateDownloadResult</a> interface that contains download information for the specified update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDownloadResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f1aa4d9-0e34-4456-bac0-2c8b08519cdc">HResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the exception code number if an exception code number is raised during a download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5c3756b1-ad1a-47c8-98ff-e8e602302662">ResultCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/02d3442e-d098-42b6-b1b1-cc2d1a815fa4">OperationResultCode</a> enumeration that specifies the result of a download.

</td>
</tr>
</table> 

