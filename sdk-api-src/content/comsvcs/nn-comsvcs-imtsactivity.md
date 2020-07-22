---
UID: NN:comsvcs.IMTSActivity
title: IMTSActivity (comsvcs.h)
description: Submits batch work through the activity created by the MTSCreateActivity function.
helpviewer_keywords: ["IMTSActivity","IMTSActivity interface [COM+]","IMTSActivity interface [COM+]","described","_cos_IMTSActivity","comsvcs/IMTSActivity","cos.imtsactivity"]
old-location: cos\imtsactivity.htm
tech.root: cos
ms.assetid: a45b29f0-d3f1-4593-9df5-4f6d617b93fa
ms.date: 12/05/2018
ms.keywords: IMTSActivity, IMTSActivity interface [COM+], IMTSActivity interface [COM+],described, _cos_IMTSActivity, comsvcs/IMTSActivity, cos.imtsactivity
f1_keywords:
- comsvcs/IMTSActivity
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
- IMTSActivity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMTSActivity interface


## -description


<p class="CCE_Message">[<b>IMTSActivity</b> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>.]

Submits batch work through the activity created by the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMTSActivity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMTSActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMTSActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">AsyncCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-bindtocurrentthread">BindToCurrentThread</a>
</td>
<td align="left" width="63%">
Binds the batch work that is submitted using <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">IMTSActivity::AsyncCall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">IMTSActivity::SynchronousCall</a> to the current single-threaded apartment (STA).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">SynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-unbindfromthread">UnbindFromThread</a>
</td>
<td align="left" width="63%">
Unbinds the batch work that is submitted using <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-asynccall">IMTSActivity::AsyncCall</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtsactivity-synchronouscall">IMTSActivity::SynchronousCall</a> from the thread on which it is running.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtscall-oncall">IMTSCall::OnCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a>
 

 

