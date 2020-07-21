---
UID: NN:comsvcs.IDispenserManager
title: IDispenserManager (comsvcs.h)
description: Connects to the dispenser manager.
helpviewer_keywords: ["IDispenserManager","IDispenserManager interface [COM+]","IDispenserManager interface [COM+]","described","_dtc_IDispenserManager_Interface","comsvcs/IDispenserManager","cos.idispensermanager"]
old-location: cos\idispensermanager.htm
tech.root: cossdk
ms.assetid: a0465d78-f8b7-4934-9dc6-c8f0ead04bf1
ms.date: 12/05/2018
ms.keywords: IDispenserManager, IDispenserManager interface [COM+], IDispenserManager interface [COM+],described, _dtc_IDispenserManager_Interface, comsvcs/IDispenserManager, cos.idispensermanager
f1_keywords:
- comsvcs/IDispenserManager
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
- IDispenserManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDispenserManager interface


## -description


Connects to the dispenser manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDispenserManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDispenserManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDispenserManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispensermanager-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Determines the current context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-idispensermanager-registerdispenser">RegisterDispenser</a>
</td>
<td align="left" width="63%">
Registers the resource dispenser with the dispenser manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>
 

 

