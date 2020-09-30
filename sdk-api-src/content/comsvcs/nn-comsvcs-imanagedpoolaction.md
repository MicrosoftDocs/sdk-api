---
UID: NN:comsvcs.IManagedPoolAction
title: IManagedPoolAction (comsvcs.h)
description: Enables an object to be notified before it is released from a COM+ object pool.
helpviewer_keywords: ["IManagedPoolAction","IManagedPoolAction interface [COM+]","IManagedPoolAction interface [COM+]","described","_cos_IManagedPoolAction","comsvcs/IManagedPoolAction","cos.imanagedpoolaction"]
old-location: cos\imanagedpoolaction.htm
tech.root: cos
ms.assetid: 6c29bbe0-840f-4eaf-97ad-40b0f89cadfd
ms.date: 12/05/2018
ms.keywords: IManagedPoolAction, IManagedPoolAction interface [COM+], IManagedPoolAction interface [COM+],described, _cos_IManagedPoolAction, comsvcs/IManagedPoolAction, cos.imanagedpoolaction
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
 - IManagedPoolAction
 - comsvcs/IManagedPoolAction
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
 - IManagedPoolAction
---

# IManagedPoolAction interface


## -description

Enables an object to be notified before it is released from a COM+ object pool.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedPoolAction</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IManagedPoolAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedPoolAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-imanagedpoolaction-lastrelease">LastRelease</a>
</td>
<td align="left" width="63%">
Called when a COM+ object pool drops the last reference to the object that implements it.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/com--object-pooling">COM+ Object Pooling</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpooledobj">IManagedPooledObj</a>