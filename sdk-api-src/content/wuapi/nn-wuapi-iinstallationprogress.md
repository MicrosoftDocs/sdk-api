---
UID: NN:wuapi.IInstallationProgress
title: IInstallationProgress (wuapi.h)
author: windows-sdk-content
description: Represents the progress of an asynchronous installation or uninstallation.
old-location: wua\iinstallationprogress.htm
tech.root: Wua_Sdk
ms.assetid: aa7e0c4d-9cb3-4473-a3b9-02ff9643f7de
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInstallationProgress, IInstallationProgress interface [Windows Update Agent], IInstallationProgress interface [Windows Update Agent],described, wua.iinstallationprogress, wuapi/IInstallationProgress
ms.topic: interface
f1_keywords: 
 - "wuapi/IInstallationProgress"
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
 - IInstallationProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationProgress interface


## -description


Represents the progress of an asynchronous installation or uninstallation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationProgress</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IInstallationProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInstallationProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationprogress-getupdateresult">GetUpdateResult</a>
</td>
<td align="left" width="63%">
Returns the result of the installation or uninstallation of a specified update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationProgress</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/aa386047(v=vs.85)">CurrentUpdateIndex</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a zero-based index value that specifies the update that is  currently being installed or uninstalled when multiple updates have been selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete">CurrentUpdatePercentComplete</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete">PercentComplete</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets how far the overall installation or uninstallation process has progressed, as a percentage.

</td>
</tr>
</table> 

