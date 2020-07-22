---
UID: NN:comsvcs.ICOMLBArguments
title: ICOMLBArguments (comsvcs.h)
description: Used to activate the COM+ component load balancing service.
helpviewer_keywords: ["ICOMLBArguments","ICOMLBArguments interface [COM+]","ICOMLBArguments interface [COM+]","described","_cos_icomlbarguments","comsvcs/ICOMLBArguments","cos.icomlbarguments"]
old-location: cos\icomlbarguments.htm
tech.root: cos
ms.assetid: 1eb1c464-9371-420e-afc0-4b18c11a70d4
ms.date: 12/05/2018
ms.keywords: ICOMLBArguments, ICOMLBArguments interface [COM+], ICOMLBArguments interface [COM+],described, _cos_icomlbarguments, comsvcs/ICOMLBArguments, cos.icomlbarguments
f1_keywords:
- comsvcs/ICOMLBArguments
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
- ICOMLBArguments
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMLBArguments interface


## -description


Used to activate the COM+ component load balancing service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMLBArguments</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICOMLBArguments</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICOMLBArguments</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomlbarguments-getclsid">GetCLSID</a>
</td>
<td align="left" width="63%">
Retrieves the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomlbarguments-getmachinename">GetMachineName</a>
</td>
<td align="left" width="63%">
Retrieves the computer name for the load balancing server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomlbarguments-setclsid">SetCLSID</a>
</td>
<td align="left" width="63%">
Sets the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomlbarguments-setmachinename">SetMachineName</a>
</td>
<td align="left" width="63%">
Sets the computer name for the load balancing server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iselectcomlbserver">ISelectCOMLBServer</a>
 

 

