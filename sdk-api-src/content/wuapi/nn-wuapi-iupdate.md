---
UID: NN:wuapi.IUpdate
title: IUpdate
author: windows-sdk-content
description: Contains the properties and methods that are available to an update.
old-location: wua\iupdate.htm
tech.root: wua_sdk
ms.assetid: d0feee2a-96f6-4c86-aaf8-f49d05616fc9
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IUpdate, IUpdate interface [Windows Update Agent], IUpdate interface [Windows Update Agent],described, wua.iupdate, wuapi/IUpdate
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
 - IUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdate interface


## -description


Contains the properties and methods that are available to an update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdate</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IUpdate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a25994-eace-45ec-8e6b-40d69796f168">AcceptEula</a>
</td>
<td align="left" width="63%">
Accepts the Microsoft Software License Terms that are associated with an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43af8bb9-0e09-4541-bc2e-fd40be64a980">CopyFromCache</a>
</td>
<td align="left" width="63%">
Copies the contents of an update into a specified path.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a27d7144-bd76-40e3-b8a7-951ae1974afb">AutoSelectOnWebSites</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the update is flagged to be automatically selected by Windows Update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17fcde27-86be-4fe1-8cd2-a49cfe2b408f">BundledUpdates</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains information about the ordered list of the bundled updates for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/45d1cdb1-6aab-4119-8cd5-a4217c9adc3e">CanRequireSource</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the source media of the update is required for installation or uninstallation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/25620fc2-25f2-4626-9e41-b44c305c505c">Categories</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains a  collection of categories to which the update belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/78f5ab06-13d1-4564-b9eb-334d4f0c34e8">Deadline</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the date by which the update must be installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b713a349-45fe-492a-a966-17112edf00ec">DeltaCompressedContentAvailable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether delta-compressed content is available on a server for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9fdb3918-9fc7-491f-9abb-4c2f13528817">DeltaCompressedContentPreferred</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether to prefer delta-compressed content during the download and install or uninstall of the update if delta-compressed content is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/52bdde0e-6b00-4bc9-8ad6-8bae5b01b7f3">DeploymentAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the action for which the update is deployed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2448c9aa-0e90-4454-b168-c31b36f569af">Description</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the localized description of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dbeeaac7-3841-42ec-a3f3-bdf94694dbef">DownloadContents</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets file information about the download contents of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a1963c34-6387-442f-847a-1348789f3b05">DownloadPriority</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the suggested download priority of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c62967c1-d72a-4ae0-ad02-94e948985b87">EulaAccepted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the Microsoft Software License Terms that are associated with the update are accepted for the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4c3ddc9c-0261-46e8-92df-d125fea46991">EulaText</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the full localized text of the Microsoft Software License Terms that are associated with the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af7d4b22-c4e2-4f3d-bef6-5a0cc4f4d5a5">HandlerID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the install handler of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e34019e4-54f4-486d-b5e7-5e65f65d1941">Identity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains the unique identifier of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0cae0b5b-8a47-461f-ab91-b9ac80418e20">Image</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains information about an image that is associated with the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f02e5ebc-a8ea-496b-a79e-52644b98e75d">InstallationBehavior</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains the installation options of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5e832ea1-1cfc-4421-aa3e-89d9ec83082f">IsBeta</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the update is a beta release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4e20f2b0-096c-4ec6-b554-1891522b8933">IsDownloaded</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether all the update content is cached on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/229fbb68-cc99-440e-89e1-b9c4e69dd0b3">IsHidden</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether an update is hidden by a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2adebe8e-554e-4337-9bbf-1d8967fefef1">IsInstalled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the update is installed on a computer when the search is performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5052914f-7b92-4637-b188-dce4a8e15328">IsMandatory</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the installation of the update is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0f67461b-3df9-45e9-95b3-d7f46fa11162">IsUninstallable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether a user can uninstall the update from a computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3f30f356-6534-40b7-b3e5-18ab2980a610">KBArticleIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of Microsoft Knowledge Base article IDs that are associated with the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/788942cc-5cfa-4ce3-bcf6-05c78a817ec8">Languages</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains the languages that are supported by the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5190ed29-5737-4100-b67c-1333bde28102">LastDeploymentChangeTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the last published date of the update,  in Coordinated Universal Time (UTC) date and time,  on the server that deploys the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/22f19d4f-e144-4b06-a428-d2133198288a">MaxDownloadSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the maximum download size of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/58666d64-fe29-4ece-8b51-67212f90e54e">MinDownloadSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the minimum download size of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8500bcf4-470d-472e-aa3a-ba424662ec41">MoreInfoUrls</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of language-specific strings that specify the hyperlinks to more information about the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ed3187c5-e175-4287-b930-2c283c9e93f3">MsrcSeverity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the Microsoft Security Response Center severity rating of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/21003be2-c14e-48d4-a51f-ed75b1b47284">RecommendedCPUSpeed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the recommended CPU speed used to install the update, in megahertz (MHz).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/958d3de3-b2e0-47e0-9a71-b12ff6669242">RecommendedHardDiskSpace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the recommended free space that should be available on the hard disk before you install the update. The free space is specified in megabytes (MB).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/68a8341b-ba0a-4694-89c3-34fefb950bf7">RecommendedMemory</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the recommended physical memory size that should be available in your  computer before you install the update. The physical memory size is specified in megabytes (MB).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b27dc2f6-c985-437f-b960-f2470c30ef0a">ReleaseNotes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the localized release notes for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/63de677b-4a0e-4ac6-937f-bf195a0da205">SecurityBulletinIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of string values that contain the security bulletin IDs that are associated with the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b819e321-3f8d-4d8f-8f6d-16792af990e5">SupersededUpdateIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of update identifiers. This collection of identifiers specifies the updates that are superseded by the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c4734e71-a64d-4231-80ed-1ee2bcc98ce1">SupportUrl</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a hyperlink to the language-specific support information for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83b1bcfc-d974-4804-8ed0-1ccde335b5ac">Title</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the localized title of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2556ee19-b6ff-4e66-9e40-2c0a1d6a0176">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the type of the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/12f35005-5dea-42c9-8c3b-eeb28bdd93b3">UninstallationBehavior</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains the uninstallation options for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e5a84291-2c50-4ede-b69b-07d5a4226164">UninstallationNotes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the uninstallation notes for the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f112ce5b-9f94-4fdc-96d8-1f216e3729d0">UninstallationSteps</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an interface that contains the uninstallation steps for  the update.

</td>
</tr>
</table> 


## -remarks



If the <a href="https://msdn.microsoft.com/17fcde27-86be-4fe1-8cd2-a49cfe2b408f">BundledUpdates</a> property contains an <a href="https://msdn.microsoft.com/e56a09e9-6a5f-4579-9a5c-987519fccaad">IUpdateCollection</a>, some properties and methods of the update may only be available on the bundled updates, for example, <a href="https://msdn.microsoft.com/dbeeaac7-3841-42ec-a3f3-bdf94694dbef">DownloadContents</a> or <a href="https://msdn.microsoft.com/43af8bb9-0e09-4541-bc2e-fd40be64a980">CopyFromCache</a>.



