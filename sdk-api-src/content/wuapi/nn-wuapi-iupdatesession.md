---
UID: NN:wuapi.IUpdateSession
title: IUpdateSession
author: windows-sdk-content
description: Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.
old-location: wua\iupdatesession.htm
old-project: Wua_Sdk
ms.assetid: 00b84246-b5f2-48c2-a0ab-eaaa1ec80262
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IUpdateSession, IUpdateSession interface [Windows Update Agent], IUpdateSession interface [Windows Update Agent],described, wua.iupdatesession, wuapi/IUpdateSession
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSession interface


## -description


Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSession</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IUpdateSession</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9d410114-2327-489c-84b6-c3f5367008c2">CreateUpdateDownloader</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5b5f760-0d25-4506-95d3-63ff4a0b9188">CreateUpdateInstaller</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7a4aa9-7952-4080-9ac0-9544f959475f">CreateUpdateSearcher</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> interface for this session.

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

<a href="https://msdn.microsoft.com/9e025c75-5884-4a45-ab11-24a8b66ab838">ClientApplicationID</a>


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

<a href="https://msdn.microsoft.com/ba1e5092-33b1-4a03-b4f5-08b435706f49">ReadOnly</a>


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

<a href="https://msdn.microsoft.com/33611ac4-9471-45c5-91cc-0a07251c74a5">WebProxy</a>


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



