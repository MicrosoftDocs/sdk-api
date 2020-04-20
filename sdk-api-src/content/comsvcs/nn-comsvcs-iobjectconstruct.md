---
UID: NN:comsvcs.IObjectConstruct
title: IObjectConstruct (comsvcs.h)
description: Controls the object construction process by passing in parameters from other methods or objects.helpviewer_keywords: ["IObjectConstruct","IObjectConstruct interface [COM+]","IObjectConstruct interface [COM+]","described","_cos_IObjectConstruct","comsvcs/IObjectConstruct","cos.iobjectconstruct"]
old-location: cos\iobjectconstruct.htm
tech.root: cossdk
ms.assetid: 3fc84c37-f38d-4ff1-bdb1-f5d298802b64
ms.date: 12/05/2018
ms.keywords: IObjectConstruct, IObjectConstruct interface [COM+], IObjectConstruct interface [COM+],described, _cos_IObjectConstruct, comsvcs/IObjectConstruct, cos.iobjectconstruct
f1_keywords:
- comsvcs/IObjectConstruct
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
- IObjectConstruct
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectConstruct interface


## -description


Controls the object construction process by passing in parameters from other methods or objects. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectConstruct</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectConstruct</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectConstruct</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectconstruct-construct">Construct</a>
</td>
<td align="left" width="63%">
Constructs an object using the specified parameters.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--object-constructor-strings">COM+ Object Constructor Strings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectconstructstring">IObjectConstructString</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/specifying-an-object-constructor-string-for-a-component">Specifying an Object Constructor String for a Component</a>
 

 

