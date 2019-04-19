---
UID: NN:vsadmin.IVssAdmin
title: IVssAdmin (vsadmin.h)
author: windows-sdk-content
description: The IVssAdmin interface manages providers registered with VSS.
old-location: base\ivssadmin.htm
tech.root: VSS
ms.assetid: 6128d627-380b-4fef-b58a-caf8f149f526
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssAdmin, IVssAdmin interface [VSS], IVssAdmin interface [VSS],described, base.ivssadmin, vsadmin/IVssAdmin
ms.topic: interface
req.header: vsadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsAdmin.h
api_name:
 - IVssAdmin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssAdmin interface


## -description


The <b>IVssAdmin</b> interface manages providers registered 
   with VSS.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssAdmin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssAdmin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssAdmin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64feae8f-c627-45b5-a3bc-0c47e9f8a4cb">AbortAllSnapshotsInProgress</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1267b715-dc2e-47a2-88f1-5c03b5fb5415">QueryProviders</a>
</td>
<td align="left" width="63%">
Queries all registered providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c17aee22-3afc-4ac5-a0c5-3fa1164ceee0">RegisterProvider</a>
</td>
<td align="left" width="63%">
Registers a new shadow copy provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d31ed47f-6850-4f4b-aea2-5171722db7db">UnregisterProvider</a>
</td>
<td align="left" width="63%">
Unregisters an existing provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

