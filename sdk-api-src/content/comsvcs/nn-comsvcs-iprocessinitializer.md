---
UID: NN:comsvcs.IProcessInitializer
title: IProcessInitializer (comsvcs.h)
description: Provides methods that can be called whenever Dllhost.exe starts up or shuts down.
helpviewer_keywords: ["IProcessInitializer","IProcessInitializer interface [COM+]","IProcessInitializer interface [COM+]","described","_cos_IProcessInitializer","comsvcs/IProcessInitializer","cos.iprocessinitializer"]
old-location: cos\iprocessinitializer.htm
tech.root: cossdk
ms.assetid: 7c7edeb7-5bc1-4ede-8fe4-78fc7c6bdd30
ms.date: 12/05/2018
ms.keywords: IProcessInitializer, IProcessInitializer interface [COM+], IProcessInitializer interface [COM+],described, _cos_IProcessInitializer, comsvcs/IProcessInitializer, cos.iprocessinitializer
f1_keywords:
- comsvcs/IProcessInitializer
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- ComSvcs.h
api_name:
- IProcessInitializer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProcessInitializer interface


## -description


Provides methods that can be called whenever Dllhost.exe starts up or shuts down.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProcessInitializer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProcessInitializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProcessInitializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iprocessinitializer-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Called when Dllhost.exe shuts down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iprocessinitializer-startup">Startup</a>
</td>
<td align="left" width="63%">
Called when Dllhost.exe starts.


</td>
</tr>
</table> 

