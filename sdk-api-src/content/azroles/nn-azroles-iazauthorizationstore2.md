---
UID: NN:azroles.IAzAuthorizationStore2
title: IAzAuthorizationStore2 (azroles.h)
author: windows-sdk-content
description: Inherits from the AzAuthorizationStore object and implements methods to create and open IAzApplication2 objects.
old-location: security\iazauthorizationstore2.htm
tech.root: SecAuthZ
ms.assetid: 8b3901a9-003f-4346-a0c7-34a1ed730949
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAzAuthorizationStore2, IAzAuthorizationStore2 interface [Security], IAzAuthorizationStore2 interface [Security],described, azroles/IAzAuthorizationStore2, security.iazauthorizationstore2
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
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
 - IAzAuthorizationStore2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzAuthorizationStore2 interface


## -description


The <b>IAzAuthorizationStore2</b> interface inherits from the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object and implements methods to create and open <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzAuthorizationStore2</b> interface inherits from <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> and <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. <b>IAzAuthorizationStore2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzAuthorizationStore2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9af40e4-9ed9-4b81-b808-315eef07a96d">CreateApplication2</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object by using the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8705ea59-2419-4af5-9cc2-591221e09073">OpenApplication2</a>
</td>
<td align="left" width="63%">
Opens the <a href="https://msdn.microsoft.com/58f0627e-fa92-4b3b-a0cd-7e437d451606">IAzApplication2</a> object by using the specified name.

</td>
</tr>
</table> 

