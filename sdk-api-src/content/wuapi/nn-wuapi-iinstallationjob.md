---
UID: NN:wuapi.IInstallationJob
title: IInstallationJob
author: windows-sdk-content
description: Contains properties and methods that are available to an installation or uninstallation operation.
old-location: wua\iinstallationjob.htm
old-project: Wua_Sdk
ms.assetid: 1a83a44e-cd3b-43b0-8741-a73fe9954063
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IInstallationJob, IInstallationJob interface [Windows Update Agent], IInstallationJob interface [Windows Update Agent],described, wua.iinstallationjob, wuapi/IInstallationJob
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
 - IInstallationJob
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IInstallationJob interface


## -description


The <b>IInstallationJob</b> interface contains properties and methods that are available to an installation or uninstallation operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationJob</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IInstallationJob</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ceb42a41-9df0-4075-afbe-f8753d4543d8">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to be completed and then releases all the callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d63ec9d-bf7a-4c5d-a1e7-4dcc0f236d07">GetProgress</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/aa7e0c4d-9cb3-4473-a3b9-02ff9643f7de">IInstallationProgress</a> interface that describes the current progress of an installation or uninstallation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efe0c51c-1193-4a25-88ae-ad74550f42ba">RequestAbort</a>
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

<a href="https://msdn.microsoft.com/ff3632de-4fb7-4e82-a642-9c9b38f4063c">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the caller-specific state object that is passed to the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/043e1f6a-993c-48be-9d91-7f99cd5712d4">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that indicates whether a call to the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method is completely processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f6a21db3-1182-4650-8502-814db88cbacb">Updates</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.

</td>
</tr>
</table> 

