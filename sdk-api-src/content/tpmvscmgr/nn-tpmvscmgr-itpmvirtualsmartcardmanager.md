---
UID: NN:tpmvscmgr.ITpmVirtualSmartCardManager
title: ITpmVirtualSmartCardManager
author: windows-sdk-content
description: Manages the TPM virtual smart cards.
old-location: security\itpmvirtualsmartcardmanager.htm
tech.root: secauthn
ms.assetid: 46CC703B-14A2-4588-BA13-837C76B70F07
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITpmVirtualSmartCardManager, ITpmVirtualSmartCardManager interface [Security], ITpmVirtualSmartCardManager interface [Security],described, security.itpmvirtualsmartcardmanager, tpmvscmgr/ITpmVirtualSmartCardManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tpmvscmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tpmvscmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vscmgr.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vscmgr.lib
 - Vscmgr.dll
api_name:
 - ITpmVirtualSmartCardManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITpmVirtualSmartCardManager interface


## -description


Manages the TPM virtual smart cards.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITpmVirtualSmartCardManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITpmVirtualSmartCardManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITpmVirtualSmartCardManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C80C4DE2-0C43-40A5-81E6-7036A0B8DEB7">CreateVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Creates a TPM virtual smart card with the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8624CBF-FC39-4269-9405-8E7B5EE88F8D">DestroyVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Destroys the TPM virtual smart card that has the given instance ID.

</td>
</tr>
</table> 

