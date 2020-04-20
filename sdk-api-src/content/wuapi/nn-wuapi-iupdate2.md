---
UID: NN:wuapi.IUpdate2
title: IUpdate2 (wuapi.h)
description: Contains the properties and methods that are available to an update.helpviewer_keywords: ["IUpdate2","IUpdate2 interface [Windows Update Agent]","IUpdate2 interface [Windows Update Agent]","described","wua.iupdate2","wuapi/IUpdate2"]
old-location: wua\iupdate2.htm
tech.root: Wua_Sdk
ms.assetid: 75041e85-0f3c-4996-9af2-d2969549393e
ms.date: 12/05/2018
ms.keywords: IUpdate2, IUpdate2 interface [Windows Update Agent], IUpdate2 interface [Windows Update Agent],described, wua.iupdate2, wuapi/IUpdate2
f1_keywords:
- wuapi/IUpdate2
dev_langs:
- c++
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
- IUpdate2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdate2 interface


## -description


Contains the  properties and methods that are available to an update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdate2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>. <b>IUpdate2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUpdate2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate2-copytocache">CopyToCache</a>
</td>
<td align="left" width="63%">
Copies files for an update from a specified source location to the internal Windows Update Agent (WUA) download cache.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdate2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate2-get_cveids">CveIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of common vulnerabilities and exposures (CVE) IDs that are associated with the update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate2-get_ispresent">IsPresent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether an update is present on a computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdate2-get_rebootrequired">RebootRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation or the uninstallation of an update.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
 

 

