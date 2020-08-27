---
UID: NN:wuapi.IAutomaticUpdatesSettings2
title: IAutomaticUpdatesSettings2 (wuapi.h)
description: Contains the settings that are available in Automatic Updates.
helpviewer_keywords: ["IAutomaticUpdatesSettings2","IAutomaticUpdatesSettings2 interface [Windows Update Agent]","IAutomaticUpdatesSettings2 interface [Windows Update Agent]","described","wua.iautomaticupdatessettings2","wuapi/IAutomaticUpdatesSettings2"]
old-location: wua\iautomaticupdatessettings2.htm
tech.root: wua
ms.assetid: 5ad1a3ee-3293-4825-a85e-ca1e3a38e775
ms.date: 12/05/2018
ms.keywords: IAutomaticUpdatesSettings2, IAutomaticUpdatesSettings2 interface [Windows Update Agent], IAutomaticUpdatesSettings2 interface [Windows Update Agent],described, wua.iautomaticupdatessettings2, wuapi/IAutomaticUpdatesSettings2
f1_keywords:
- wuapi/IAutomaticUpdatesSettings2
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
- IAutomaticUpdatesSettings2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutomaticUpdatesSettings2 interface


## -description


Contains the settings that are available in Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>. <b>IAutomaticUpdatesSettings2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAutomaticUpdatesSettings2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission">CheckPermission</a>
</td>
<td align="left" width="63%">
Determines whether a specific user or type of user has permission to perform a selected action.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates">IncludeRecommendedUpdates</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a  search for updates and installation of updates is performed.

</td>
</tr>
</table> 


## -remarks



The <b>IAutomaticUpdatesSettings2</b> interface  may require you to update the Windows Update Agent (WUA). For more information, see <a href="https://docs.microsoft.com/windows/desktop/Wua_Sdk/updating-the-windows-update-agent">Updating Windows Update Agent</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iautomaticupdatessettings">IAutomaticUpdatesSettings</a>
 

 

