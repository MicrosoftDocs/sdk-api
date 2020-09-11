---
UID: NN:comsvcs.ObjectControl
title: ObjectControl (comsvcs.h)
description: If you implement this interface in your component, the COM+ run-time environment automatically calls its methods on your objects at the appropriate times.
helpviewer_keywords: ["ObjectControl","ObjectControl interface [COM+]","ObjectControl interface [COM+]","described","_cos_ObjectControl","comsvcs/ObjectControl","cos.objectcontrol"]
old-location: cos\objectcontrol.htm
tech.root: cos
ms.assetid: 3ca939de-31ce-4ce6-84cd-4b4191a0753c
ms.date: 12/05/2018
ms.keywords: ObjectControl, ObjectControl interface [COM+], ObjectControl interface [COM+],described, _cos_ObjectControl, comsvcs/ObjectControl, cos.objectcontrol
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ObjectControl
 - comsvcs/ObjectControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ObjectControl
---

# ObjectControl interface


## -description

If you implement this interface in your component, the COM+ run-time environment automatically calls its methods on your objects at the appropriate times. Only the COM+ run-time environment can invoke the <b>ObjectControl</b> methods; they are not accessible to an object's clients or to the object itself. If a client queries for the <b>ObjectControl</b> interface, <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> returns E_NOINTERFACE.

<b>ObjectControl</b> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a> provide the same functionality, but unlike <b>IObjectControl</b>, <b>ObjectControl</b> is compatible with Automation.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ObjectControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ObjectControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ObjectControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-activate">Activate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform context-specific initialization whenever it is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-canbepooled">CanBePooled</a>
</td>
<td align="left" width="63%">
Indicates whether the object can be pooled for reuse when it is deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-objectcontrol-deactivate">Deactivate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform cleanup required before it is recycled or destroyed.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/context-activation">Context Activation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontrol">IObjectControl</a>

