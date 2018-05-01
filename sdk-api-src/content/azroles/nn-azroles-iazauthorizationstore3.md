---
UID: NN:azroles.IAzAuthorizationStore3
title: IAzAuthorizationStore3
author: windows-driver-content
description: Extends the IAzAuthorizationStore2 interface with methods that manage business rule (BizRule) support and caching.
old-location: security\iazauthorizationstore3.htm
old-project: SecAuthZ
ms.assetid: 7063416c-b132-4b3a-bb2b-d27fccea25e4
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IAzAuthorizationStore3, IAzAuthorizationStore3 interface [Security], IAzAuthorizationStore3 interface [Security], described, azroles/IAzAuthorizationStore3, security.iazauthorizationstore3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzAuthorizationStore3
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore3 interface


## -description


The <b>IAzAuthorizationStore3</b> interface extends the <a href="https://msdn.microsoft.com/8b3901a9-003f-4346-a0c7-34a1ed730949">IAzAuthorizationStore2</a> interface with methods that manage business rule (BizRule) support and caching.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore3</b> interface inherits from <a href="https://msdn.microsoft.com/8b3901a9-003f-4346-a0c7-34a1ed730949">IAzAuthorizationStore2</a>. <b>IAzAuthorizationStore3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/88449b12-5086-4f86-94d4-2a4afb4be070">BizruleGroupSupported</a>
</td>
<td align="left" width="63%">
Returns a Boolean value that specifies whether this <b>IAzAuthorizationStore3</b> object supports application groups that use BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/263d8f04-8ed9-4801-86cf-51ede83436c7">GetSchemaVersion</a>
</td>
<td align="left" width="63%">
Gets the version number of this authorization store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b5bed8f-f38a-46dd-b889-65d43b13ce7c">IsFunctionalLevelUpgradeSupported</a>
</td>
<td align="left" width="63%">
Gets a Boolean  value that indicates whether the version of this authorization store can be upgraded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b5bed8f-f38a-46dd-b889-65d43b13ce7c">IsUpdateNeeded</a>
</td>
<td align="left" width="63%">
Checks whether the persisted version of this authorization store is newer than the cached version. If the cached version of the store is newer, the calling application can update the cached version by calling the <a href="https://msdn.microsoft.com/1fd17040-f736-44a6-8a01-720f4c8fe9ac">UpdateCache</a> method of the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7719e3fd-5b06-468c-9034-f1f0bb41a5be">UpgradeStoresFunctionalLevel</a>
</td>
<td align="left" width="63%">
Upgrades this authorization store from version 1 to version 2.

</td>
</tr>
</table> 

