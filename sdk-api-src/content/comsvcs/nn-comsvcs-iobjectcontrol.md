---
UID: NN:comsvcs.IObjectControl
title: IObjectControl (comsvcs.h)
author: windows-sdk-content
description: Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.
old-location: cos\iobjectcontrol.htm
tech.root: cossdk
ms.assetid: cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjectControl, IObjectControl interface [COM+], IObjectControl interface [COM+],described, _cos_IObjectControl, comsvcs/IObjectControl, cos.iobjectcontrol
ms.topic: interface
f1_keywords: 
 - "comsvcs/IObjectControl"
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
 - IObjectControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectControl interface


## -description


Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-activate">Activate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform context-specific initialization whenever it is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-canbepooled">CanBePooled</a>
</td>
<td align="left" width="63%">
Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontrol-deactivate">Deactivate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform required cleanup before it is recycled or destroyed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/context-activation">Context Activation</a>
 

 

