---
UID: NN:wuapi.IUpdateDownloader
title: IUpdateDownloader (wuapi.h)
description: Downloads updates from the server.
helpviewer_keywords: ["IUpdateDownloader","IUpdateDownloader interface [Windows Update Agent]","IUpdateDownloader interface [Windows Update Agent]","described","wua.iupdatedownloader","wuapi/IUpdateDownloader"]
old-location: wua\iupdatedownloader.htm
tech.root: wua
ms.assetid: 8f9f3430-fc78-46cb-9dc8-b97e9d35d91c
ms.date: 12/05/2018
ms.keywords: IUpdateDownloader, IUpdateDownloader interface [Windows Update Agent], IUpdateDownloader interface [Windows Update Agent],described, wua.iupdatedownloader, wuapi/IUpdateDownloader
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
 - IUpdateDownloader
 - wuapi/IUpdateDownloader
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
 - IUpdateDownloader
---

# IUpdateDownloader interface


## -description

Downloads updates from the server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateDownloader</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateDownloader</b> also has these types of members:
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
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">BeginDownload</a>
</td>
<td align="left" width="63%">
Starts an asynchronous download of the content files that are associated with the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-download">Download</a>
</td>
<td align="left" width="63%">
Starts a synchronous download of the content files that are associated with the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-enddownload">EndDownload</a>
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

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid">ClientApplicationID</a>


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

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-get_isforced">IsForced</a>


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

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-get_priority">Priority</a>


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

<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-get_updates">Updates</a>


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

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>