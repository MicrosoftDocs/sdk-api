---
UID: NN:comsvcs.IMTSCall
title: IMTSCall (comsvcs.h)
description: Implements the batch work that is submitted through the activity created by the MTSCreateActivity function.helpviewer_keywords: ["IMTSCall","IMTSCall interface [COM+]","IMTSCall interface [COM+]","described","_cos_IMTSCall","comsvcs/IMTSCall","cos.imtscall"]
old-location: cos\imtscall.htm
tech.root: cossdk
ms.assetid: dccf53c3-19d9-435b-91b7-98e41bd48e29
ms.date: 12/05/2018
ms.keywords: IMTSCall, IMTSCall interface [COM+], IMTSCall interface [COM+],described, _cos_IMTSCall, comsvcs/IMTSCall, cos.imtscall
f1_keywords:
- comsvcs/IMTSCall
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
- IMTSCall
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMTSCall interface


## -description


<p class="CCE_Message">[<b>IMTSCall</b> is available for use in the operating systems specified in the Requirements section. It may be altered of unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>.]

Implements the batch work that is submitted through the activity created by the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMTSCall</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMTSCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMTSCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtscall-oncall">OnCall</a>
</td>
<td align="left" width="63%">
Triggers the execution of the batch work implemented in this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a>
 

 

