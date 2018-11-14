---
UID: NN:azroles.IAzApplication2
title: IAzApplication2
author: windows-sdk-content
description: Inherits from the IAzApplication interface and implements additional methods to initialize IAzClientContext2 objects.
old-location: security\iazapplication2.htm
tech.root: secauthz
ms.assetid: 58f0627e-fa92-4b3b-a0cd-7e437d451606
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IAzApplication2, IAzApplication2 interface [Security], IAzApplication2 interface [Security],described, azroles/IAzApplication2, security.iazapplication2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IAzApplication2
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication2 interface


## -description


The <b>IAzApplication2</b> interface inherits from the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> interface and implements additional methods to initialize <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzApplication2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> and <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a>. <b>IAzApplication2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAzApplication2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8790ebb0-97eb-47a0-b975-87e0524dcc1b">InitializeClientContext2</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f77b5eb1-c121-4392-a317-7021059268ed">InitializeClientContextFromToken2</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object pointer from the specified client token.

</td>
</tr>
</table> 

