---
UID: NN:wuapi.IUpdate
title: IUpdate (wuapi.h)
author: windows-sdk-content
description: Contains the properties and methods that are available to an update.
old-location: wua\iupdate.htm
tech.root: Wua_Sdk
ms.assetid: d0feee2a-96f6-4c86-aaf8-f49d05616fc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdate, IUpdate interface [Windows Update Agent], IUpdate interface [Windows Update Agent],described, wua.iupdate, wuapi/IUpdate
ms.topic: interface
f1_keywords: 
 - "wuapi/IUpdate"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdate interface


## -description


Contains the properties and methods that are available to an update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdate</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUpdate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-accepteula">AcceptEula</a>
</td>
<td align="left" width="63%">
Accepts the Microsoft Software License Terms that are associated with an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-copyfromcache">CopyFromCache</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_autoselectonwebsites">AutoSelectOnWebSites</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_bundledupdates">BundledUpdates</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_canrequiresource">CanRequireSource</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_categories">Categories</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_deadline">Deadline</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_deltacompressedcontentavailable">DeltaCompressedContentAvailable</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_deltacompressedcontentpreferred">DeltaCompressedContentPreferred</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_deploymentaction">DeploymentAction</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_description">Description</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_downloadcontents">DownloadContents</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_downloadpriority">DownloadPriority</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_eulaaccepted">EulaAccepted</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_eulatext">EulaText</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_handlerid">HandlerID</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_identity">Identity</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_image">Image</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_installationbehavior">InstallationBehavior</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_isbeta">IsBeta</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_isdownloaded">IsDownloaded</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_ishidden">IsHidden</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_isinstalled">IsInstalled</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_ismandatory">IsMandatory</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_isuninstallable">IsUninstallable</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_kbarticleids">KBArticleIDs</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_languages">Languages</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_lastdeploymentchangetime">LastDeploymentChangeTime</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_maxdownloadsize">MaxDownloadSize</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_mindownloadsize">MinDownloadSize</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_moreinfourls">MoreInfoUrls</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_msrcseverity">MsrcSeverity</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedcpuspeed">RecommendedCPUSpeed</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedharddiskspace">RecommendedHardDiskSpace</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_recommendedmemory">RecommendedMemory</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_releasenotes">ReleaseNotes</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_securitybulletinids">SecurityBulletinIDs</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_supersededupdateids">SupersededUpdateIDs</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_supporturl">SupportUrl</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_title">Title</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_type">Type</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_uninstallationbehavior">UninstallationBehavior</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_uninstallationnotes">UninstallationNotes</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_uninstallationsteps">UninstallationSteps</a>


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



If the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_bundledupdates">BundledUpdates</a> property contains an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatecollection">IUpdateCollection</a>, some properties and methods of the update may only be available on the bundled updates, for example, <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-get_downloadcontents">DownloadContents</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate-copyfromcache">CopyFromCache</a>.



