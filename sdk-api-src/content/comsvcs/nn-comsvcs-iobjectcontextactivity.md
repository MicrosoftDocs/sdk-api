---
UID: NN:comsvcs.IObjectContextActivity
title: IObjectContextActivity (comsvcs.h)
description: Retrieves the activity identifier associated with the current object context.
old-location: cos\iobjectcontextactivity.htm
tech.root: cossdk
ms.assetid: b3cdd835-60fd-414c-9b60-b15c07b11f34
ms.date: 12/05/2018
ms.keywords: IObjectContextActivity, IObjectContextActivity interface [COM+], IObjectContextActivity interface [COM+],described, _cos_IObjectContextActivity, comsvcs/IObjectContextActivity, cos.iobjectcontextactivity
ms.topic: interface
f1_keywords:
- comsvcs/IObjectContextActivity
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
- IObjectContextActivity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectContextActivity interface


## -description


Retrieves the activity identifier associated with the current object context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextActivity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectContextActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectContextActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iobjectcontextactivity-getactivityid">GetActivityID</a>
</td>
<td align="left" width="63%">
Retrieves the GUID associated with the current activity.

</td>
</tr>
</table> 


## -remarks



You obtain a reference to an object's <b>IObjectContextActivity</b> interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the object's context, as in the following example:

<pre class="syntax" xml:space="preserve"><code>hr = m_pIObjectContext-&gt;QueryInterface(
            IID_IObjectContextActivity, 
            (void**)&amp;m_pIObjectContextActivity);
</code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
 

 

