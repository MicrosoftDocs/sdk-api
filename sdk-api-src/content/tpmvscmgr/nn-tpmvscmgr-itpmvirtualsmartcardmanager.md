---
UID: NN:tpmvscmgr.ITpmVirtualSmartCardManager
title: ITpmVirtualSmartCardManager (tpmvscmgr.h)
author: windows-sdk-content
description: Manages the TPM virtual smart cards.
old-location: security\itpmvirtualsmartcardmanager.htm
tech.root: SecAuthN
ms.assetid: 46CC703B-14A2-4588-BA13-837C76B70F07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITpmVirtualSmartCardManager, ITpmVirtualSmartCardManager interface [Security], ITpmVirtualSmartCardManager interface [Security],described, security.itpmvirtualsmartcardmanager, tpmvscmgr/ITpmVirtualSmartCardManager
ms.topic: interface
f1_keywords: ["tpmvscmgr/ITpmVirtualSmartCardManager"]
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
ms.custom: 19H1
---

# ITpmVirtualSmartCardManager interface


## -description


Manages the TPM virtual smart cards.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITpmVirtualSmartCardManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITpmVirtualSmartCardManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/nf-tpmvscmgr-itpmvirtualsmartcardmanager-createvirtualsmartcard">CreateVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Creates a TPM virtual smart card with the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tpmvscmgr/nf-tpmvscmgr-itpmvirtualsmartcardmanager-destroyvirtualsmartcard">DestroyVirtualSmartCard</a>
</td>
<td align="left" width="63%">
Destroys the TPM virtual smart card that has the given instance ID.

</td>
</tr>
</table> 

