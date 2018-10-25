---
UID: NN:tsgpolicyengine.ITSGPolicyEngine
title: ITSGPolicyEngine
author: windows-sdk-content
description: Exposes methods that authorize connections and resources.
old-location: termserv\itsgpolicyengine.htm
tech.root: termserv
ms.assetid: 1972032f-48ac-4a15-98ce-9349fa158a07
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ITSGPolicyEngine, ITSGPolicyEngine interface [Remote Desktop Services], ITSGPolicyEngine interface [Remote Desktop Services],described, termserv.itsgpolicyengine, tsgpolicyengine/ITSGPolicyEngine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGPolicyEngine.h
api_name:
 - ITSGPolicyEngine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSGPolicyEngine interface


## -description


Exposes methods that authorize connections and resources. Implement this interface when you want to override the default authorization logic of Remote Desktop Gateway (RD Gateway).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSGPolicyEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITSGPolicyEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSGPolicyEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41a61eef-c8fe-4e08-b793-a58553f31646">AuthorizeConnection</a>
</td>
<td align="left" width="63%">
Determines whether the specified connection is authorized to connect to  RD Gateway.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77950541-c94a-4035-a2d8-a6014eb387e5">AuthorizeResource</a>
</td>
<td align="left" width="63%">
Determines which resources the specified connection is authorized to connect to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e63b99ba-068f-4842-b00a-9bfc5f8dac73">IsQuarantineEnabled</a>
</td>
<td align="left" width="63%">
Indicates whether the authorization plug-in requires a statement of health (SoH) from the user's computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29432884-c844-4c38-92e6-e1bcbba32b2b">Refresh</a>
</td>
<td align="left" width="63%">
This method is reserved.

</td>
</tr>
</table> 

