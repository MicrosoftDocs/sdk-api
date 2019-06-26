---
UID: NN:azroles.IAzAuthorizationStore3
title: IAzAuthorizationStore3 (azroles.h)
author: windows-sdk-content
description: Extends the IAzAuthorizationStore2 interface with methods that manage business rule (BizRule) support and caching.
old-location: security\iazauthorizationstore3.htm
tech.root: SecAuthZ
ms.assetid: 7063416c-b132-4b3a-bb2b-d27fccea25e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore3, IAzAuthorizationStore3 interface [Security], IAzAuthorizationStore3 interface [Security],described, azroles/IAzAuthorizationStore3, security.iazauthorizationstore3
ms.topic: interface
f1_keywords: 
 - "azroles/IAzAuthorizationStore3"
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzAuthorizationStore3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzAuthorizationStore3 interface


## -description


The <b>IAzAuthorizationStore3</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore2">IAzAuthorizationStore2</a> interface with methods that manage business rule (BizRule) support and caching.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore2">IAzAuthorizationStore2</a>. <b>IAzAuthorizationStore3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzAuthorizationStore3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-bizrulegroupsupported">BizruleGroupSupported</a>
</td>
<td align="left" width="63%">
Returns a Boolean value that specifies whether this <b>IAzAuthorizationStore3</b> object supports application groups that use BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-getschemaversion">GetSchemaVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of this authorization store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-isupdateneeded">IsFunctionalLevelUpgradeSupported</a>
</td>
<td align="left" width="63%">
Gets a Boolean  value that indicates whether the version of this authorization store can be upgraded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-isupdateneeded">IsUpdateNeeded</a>
</td>
<td align="left" width="63%">
Checks whether the persisted version of this authorization store is newer than the cached version. If the cached version of the store is newer, the calling application can update the cached version by calling the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-updatecache">UpdateCache</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazauthorizationstore">AzAuthorizationStore</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore3-upgradestoresfunctionallevel">UpgradeStoresFunctionalLevel</a>
</td>
<td align="left" width="63%">
Upgrades this authorization store from version 1 to version 2.

</td>
</tr>
</table> 

