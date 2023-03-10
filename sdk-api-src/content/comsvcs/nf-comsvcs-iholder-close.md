---
UID: NF:comsvcs.IHolder.Close
title: IHolder::Close (comsvcs.h)
description: Closes the Holder.
helpviewer_keywords: ["Close","Close method [COM+]","Close method [COM+]","IHolder interface","IHolder interface [COM+]","Close method","IHolder.Close","IHolder::Close","_dtc_IHolder_Close","comsvcs/IHolder::Close","cos.iholder_close"]
old-location: cos\iholder_close.htm
tech.root: cos
ms.assetid: c8aac9b4-04d7-46a7-9b77-5f7d9d6a2ac3
ms.date: 12/05/2018
ms.keywords: Close, Close method [COM+], Close method [COM+],IHolder interface, IHolder interface [COM+],Close method, IHolder.Close, IHolder::Close, _dtc_IHolder_Close, comsvcs/IHolder::Close, cos.iholder_close
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
 - IHolder::Close
 - comsvcs/IHolder::Close
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
 - IHolder.Close
---

# IHolder::Close


## -description

Closes the Holder.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This closes a Resource Dispenser's Holder, after which the Resource Dispenser probably released.

Before closing, any remaining inventory is destroyed by calling back to the Resource Dispenser's <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresource">IDispenserDriver::DestroyResource</a> method.



The following sequence describes how to close down a Resource Dispenser:

<ol>
<li>Obtain a reference to the Resource Dispenser (the object that exposes <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>).
</li>
<li>Call a method in Resource Dispenser whose implementation calls <b>IHolder::Close</b>.
</li>
<li><b>IHolder::Close</b> destroys any remaining inventory by calling back to Resource Dispenser's <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresource">IDispenserDriver::DestroyResource</a> method.
</li>
<li><b>IHolder::Close</b> calls the Dispenser Manager to remove this Holder from the Holder list. (If no Holders remain, the Dispenser Manager object deletes itself.)
</li>
<li><b>IHolder::Close</b> releases its reference to Resource Dispenser's <a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a> interface. This is the reason you need a reference in step 1; otherwise, the Resource Dispenser would delete itself prematurely before the subsequent steps can be completed.
</li>
<li><b>IHolder::Close</b> returns to the Resource Dispenser.
</li>
<li>The Resource Dispenser calls <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresource">IDispenserDriver::DestroyResource</a>. The Holder now deletes itself.
</li>
<li>The method called in step 2 now returns.
</li>
<li>Release your final reference to the Resource Dispenser, which now deletes itself.
</li>
</ol>
Note that the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispensermanager-registerdispenser">IDispenserManager::RegisterDispenser</a> method does not call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> on its <i>pDispenserDriver</i> object, but <b>IHolder::Close</b> does perform a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on <i>pDispenserDriver</i>. This can cause the Resource Dispenser object to be destroyed prematurely. To prevent this premature destruction, the caller of <b>IHolder::Close</b> must hold a reference to the Resource Dispenser object as described in steps 1 and 5.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>
