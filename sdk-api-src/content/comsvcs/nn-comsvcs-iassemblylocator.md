---
UID: NN:comsvcs.IAssemblyLocator
title: IAssemblyLocator (comsvcs.h)
description: Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.
helpviewer_keywords: ["IAssemblyLocator","IAssemblyLocator interface [COM+]","IAssemblyLocator interface [COM+]","described","_cos_IAssemblyLocator","comsvcs/IAssemblyLocator","cos.iassemblylocator"]
old-location: cos\iassemblylocator.htm
tech.root: cos
ms.assetid: 347a209e-be6f-42a9-978f-f40e628fc34b
ms.date: 12/05/2018
ms.keywords: IAssemblyLocator, IAssemblyLocator interface [COM+], IAssemblyLocator interface [COM+],described, _cos_IAssemblyLocator, comsvcs/IAssemblyLocator, cos.iassemblylocator
f1_keywords:
- comsvcs/IAssemblyLocator
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
- ComSvcs.h
api_name:
- IAssemblyLocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssemblyLocator interface


## -description


Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyLocator</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAssemblyLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssemblyLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iassemblylocator-getmodules">GetModules</a>
</td>
<td align="left" width="63%">
Used to get the names of the modules that are contained in an assembly.

</td>
</tr>
</table> 

