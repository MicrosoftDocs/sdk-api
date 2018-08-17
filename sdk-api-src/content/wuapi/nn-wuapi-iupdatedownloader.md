---
UID: NN:wuapi.IUpdateDownloader
title: IUpdateDownloader
author: windows-sdk-content
description: Downloads updates from the server.
old-location: wua\iupdatedownloader.htm
old-project: wua_sdk
ms.assetid: 8f9f3430-fc78-46cb-9dc8-b97e9d35d91c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUpdateDownloader, IUpdateDownloader interface [Windows Update Agent], IUpdateDownloader interface [Windows Update Agent],described, wua.iupdatedownloader, wuapi/IUpdateDownloader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateDownloader
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateDownloader interface


## -description


Downloads updates from the server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateDownloader</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUpdateDownloader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateDownloader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">BeginDownload</a>
</td>
<td align="left" width="63%">
Starts an asynchronous download of the content files that are associated with the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b860632-3d10-4791-b4b3-d37aad319a0a">Download</a>
</td>
<td align="left" width="63%">
Starts a synchronous download of the content files that are associated with the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b89ec12a-8a51-46e6-9911-2535abc3925b">EndDownload</a>
</td>
<td align="left" width="63%">
Completes an asynchronous download.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateDownloader</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/97feda21-b592-49af-8c3a-90abd086c190">ClientApplicationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the current client application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e1ac3da4-341c-4a4e-920f-b84af03e324e">IsForced</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether the  Windows Update Agent (WUA) forces the download of  updates that are already installed or that cannot be installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d9dbaabe-7769-4a1b-8540-401b1caba372">Priority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the priority level of the download.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7c0444be-a9eb-461a-858e-1dea670afd06">Updates</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets an interface that contains a read-only collection of the updates that are specified for download.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateDownloader coclass. Use the Microsoft.Update.Downloader program identifier to create the object.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

