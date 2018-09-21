---
UID: NN:wuapi.IUpdateInstaller
title: IUpdateInstaller
author: windows-sdk-content
description: Installs or uninstalls updates from or onto a computer.
old-location: wua\iupdateinstaller.htm
tech.root: wua_sdk
ms.assetid: 7f1c272f-73ef-43ee-b1ac-ef97a4791313
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IUpdateInstaller, IUpdateInstaller interface [Windows Update Agent], IUpdateInstaller interface [Windows Update Agent],described, IUpdateInstaller interface [Windows Update Services], IUpdateInstaller interface [Windows Update Services],described, wua.iupdateinstaller, wuapi/IUpdateInstaller
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
 - IUpdateInstaller
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateInstaller interface


## -description


Installs or uninstalls updates from or onto a computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateInstaller</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IUpdateInstaller</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdateInstaller</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">BeginInstall</a>
</td>
<td align="left" width="63%">
Starts an asynchronous installation of the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">BeginUninstall</a>
</td>
<td align="left" width="63%">
Starts an asynchronous uninstallation of the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7137164c-2b82-48dc-8488-6c8872896a39">EndInstall</a>
</td>
<td align="left" width="63%">
Completes an asynchronous installation of the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a035f566-7ec6-41d5-b5b4-69c2acaa8aae">EndUninstall</a>
</td>
<td align="left" width="63%">
Completes an asynchronous uninstallation of the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009fc238-fcc4-4131-b770-9f0d0946e741">Install</a>
</td>
<td align="left" width="63%">
Starts a synchronous installation of the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/006d95ab-45bc-4110-abd9-e39de58b8a4c">RunWizard</a>
</td>
<td align="left" width="63%">
Starts a wizard that guides the local user through the steps to install the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd00fc89-077e-4897-a7ec-d2e06167b7b0">Uninstall</a>
</td>
<td align="left" width="63%">
Starts a synchronous uninstallation of the updates.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateInstaller</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6975fdc7-48db-4e34-986b-5504687fc53f">AllowSourcePrompts</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether to show source prompts to the user when installing the updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b6fba06a-1eaa-4cf6-b218-29b790e80de1">ClientApplicationID</a>


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

<a href="https://msdn.microsoft.com/20875312-f54a-45fc-a0f4-ed17b812dd9e">IsBusy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether an installation or uninstallation is in progress on a computer at a specific time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/80a30a21-9369-44bb-984a-2fdf2c1810e4">IsForced</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether  to  forcibly install or uninstall an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6862ad8c-e1fa-4880-8800-88f485b7cebf">ParentHwnd</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a handle to the parent window that can contain a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/06eb4761-3a37-44bc-82b9-b40c0595fe49">ParentWindow</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the interface that represents the parent window that can contain a dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ea74de9d-9e09-48c0-9653-c6e593f6497c">RebootRequiredBeforeInstallation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether a system restart is required before installing or uninstalling updates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f56121fd-f8ba-48b5-840b-1a5a751e1a70">Updates</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets an interface that contains a read-only collection of the updates that are specified for installation or uninstallation.

</td>
</tr>
</table> 


## -remarks



This interface can be instantiated by using the UpdateInstaller coclass. Use the Microsoft.Update.Installer program identifier to create the object.




## -see-also




<a href="https://msdn.microsoft.com/89edc91d-59a1-4e23-9adb-fc3027e2e898">IUpdateInstaller2</a>
 

 

