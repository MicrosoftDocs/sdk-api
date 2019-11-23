---
UID: NN:docobj.IContinueCallback
title: IContinueCallback (docobj.h)

description: Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.
old-location: com\icontinuecallback.htm
tech.root: com
ms.assetid: 55c960be-48e3-42e1-b459-49227be62171

ms.date: 12/05/2018
ms.keywords: IContinueCallback, IContinueCallback interface [COM], IContinueCallback interface [COM],described, _com_icontinuecallback, com.icontinuecallback, docobj/IContinueCallback
ms.topic: interface
f1_keywords: 
 - "docobj/IContinueCallback"
dev_langs:
 - c++
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
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
 - DocObj.h
api_name:
 - IContinueCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContinueCallback interface


## -description


Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.

The <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinue">FContinue</a> method is a generic continuation request. <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinueprinting">FContinuePrinting</a> carries extra information pertaining to a printing process and is used in the context of <a href="https://docs.microsoft.com/windows/desktop/api/docobj/nn-docobj-iprint">IPrint</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContinueCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContinueCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContinueCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinue">FContinue</a>
</td>
<td align="left" width="63%">
Indicates whether a generic operation should continue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/docobj/nf-docobj-icontinuecallback-fcontinueprinting">FContinuePrinting</a>
</td>
<td align="left" width="63%">
Indicates whether a lengthy printing operation should continue.

</td>
</tr>
</table> 

