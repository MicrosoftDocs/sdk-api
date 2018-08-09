---
UID: NN:azroles.IAzNameResolver
title: IAzNameResolver
author: windows-sdk-content
description: Translates security identifiers (SIDs) into principal display names.
old-location: security\iaznameresolver.htm
old-project: secauthz
ms.assetid: 9426a623-cefc-43ed-9987-77802fce1a78
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAzNameResolver, IAzNameResolver interface [Security], IAzNameResolver interface [Security],described, azroles/IAzNameResolver, security.iaznameresolver
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzNameResolver
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzNameResolver interface


## -description


The <b>IAzNameResolver</b> interface translates <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) into principal display names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzNameResolver</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzNameResolver</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzNameResolver</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3518e620-85cf-4bae-8366-d43564535774">NameFromSid</a>
</td>
<td align="left" width="63%">
Gets the display name that corresponds to the specified SID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fedf0164-51ca-480c-8e45-443e74fc5b13">NamesFromSids</a>
</td>
<td align="left" width="63%">
Gets the display names that correspond to the specified SIDs.

</td>
</tr>
</table> 

