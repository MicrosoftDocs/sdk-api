---
UID: NN:wuapi.IInstallationJob
title: IInstallationJob (wuapi.h)
author: windows-sdk-content
description: Contains properties and methods that are available to an installation or uninstallation operation.
old-location: wua\iinstallationjob.htm
tech.root: Wua_Sdk
ms.assetid: 1a83a44e-cd3b-43b0-8741-a73fe9954063
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInstallationJob, IInstallationJob interface [Windows Update Agent], IInstallationJob interface [Windows Update Agent],described, wua.iinstallationjob, wuapi/IInstallationJob
ms.topic: interface
f1_keywords: 
 - "wuapi/IInstallationJob"
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
 - IInstallationJob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationJob interface


## -description


The <b>IInstallationJob</b> interface contains properties and methods that are available to an installation or uninstallation operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationJob</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IInstallationJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInstallationJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-cleanup">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to be completed and then releases all the callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-getprogress">GetProgress</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogress">IInstallationProgress</a> interface that describes the current progress of an installation or uninstallation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-requestabort">RequestAbort</a>
</td>
<td align="left" width="63%">
Makes a request to cancel an installation or uninstallation.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-get_asyncstate">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the caller-specific state object that is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-get_iscompleted">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that indicates whether a call to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> method is completely processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationjob-get_updates">Updates</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.

</td>
</tr>
</table> 

