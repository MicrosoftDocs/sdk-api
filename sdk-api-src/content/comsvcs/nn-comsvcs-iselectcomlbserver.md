---
UID: NN:comsvcs.ISelectCOMLBServer
title: ISelectCOMLBServer (comsvcs.h)
description: Activates the COM+ component load balancing service.helpviewer_keywords: ["ISelectCOMLBServer","ISelectCOMLBServer interface [COM+]","ISelectCOMLBServer interface [COM+]","described","_cos_ISelectCOMLBServer","comsvcs/ISelectCOMLBServer","cos.iselectcomlbserver"]
old-location: cos\iselectcomlbserver.htm
tech.root: cossdk
ms.assetid: ce2edece-6375-4101-b288-c250fb21cfb7
ms.date: 12/05/2018
ms.keywords: ISelectCOMLBServer, ISelectCOMLBServer interface [COM+], ISelectCOMLBServer interface [COM+],described, _cos_ISelectCOMLBServer, comsvcs/ISelectCOMLBServer, cos.iselectcomlbserver
f1_keywords:
- comsvcs/ISelectCOMLBServer
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
- ISelectCOMLBServer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISelectCOMLBServer interface


## -description


Activates the COM+ component load balancing service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISelectCOMLBServer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISelectCOMLBServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISelectCOMLBServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iselectcomlbserver-getlbserver">GetLBServer</a>
</td>
<td align="left" width="63%">
Retrieves the name of  the load balancing server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iselectcomlbserver-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the load balancing server object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomlbarguments">ICOMLBArguments</a>
 

 

