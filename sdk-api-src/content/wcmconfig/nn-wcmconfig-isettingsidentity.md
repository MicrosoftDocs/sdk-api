---
UID: NN:wcmconfig.ISettingsIdentity
title: ISettingsIdentity
author: windows-driver-content
description: Identifies a namespace to open or use.
old-location: smi\isettingsidentity.htm
old-project: SMI
ms.assetid: aa9d5604-5b94-47d9-9e68-d708a656a5ea
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISettingsIdentity, ISettingsIdentity interface [SMI], ISettingsIdentity interface [SMI],described, smi.isettingsidentity, wcmconfig/ISettingsIdentity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsIdentity
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsIdentity interface


## -description


Identifies a namespace to open or use.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsIdentity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsIdentity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsIdentity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d79bf4be-f3ed-426b-a880-b9ab8aee0092">GetAttribute</a>
</td>
<td align="left" width="63%">
Gets the identity attribute for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the identity flags for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/498bb364-3da8-456d-8e77-22b508516de0">SetAttribute</a>
</td>
<td align="left" width="63%">
Sets the identity attribute for a setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556703">SetFlags</a>
</td>
<td align="left" width="63%">
 Sets the identity flags for a setting.

</td>
</tr>
</table> 

