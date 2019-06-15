---
UID: NN:wuapi.IUpdateSession
title: IUpdateSession (wuapi.h)
author: windows-sdk-content
description: Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.
old-location: wua\iupdatesession.htm
tech.root: Wua_Sdk
ms.assetid: 00b84246-b5f2-48c2-a0ab-eaaa1ec80262
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateSession, IUpdateSession interface [Windows Update Agent], IUpdateSession interface [Windows Update Agent],described, wua.iupdatesession, wuapi/IUpdateSession
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
 - IUpdateSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateSession interface


## -description


Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSession</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdateSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatedownloader">CreateUpdateDownloader</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatedownloader">IUpdateDownloader</a> interface for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdateinstaller">CreateUpdateInstaller</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> interface for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-createupdatesearcher">CreateUpdateSearcher</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface for this session.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSession</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-get_clientapplicationid">ClientApplicationID</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Identifies the current client application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-get_readonly">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the session object is read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession-get_webproxy">WebProxy</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the proxy settings that are used to access the server.

</td>
</tr>
</table> 


## -remarks



You can create an instance of this interface by using the UpdateSession coclass. Use the Microsoft.Update.Session program identifier to create the object.



