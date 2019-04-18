---
UID: NN:docobj.IContinueCallback
title: IContinueCallback (docobj.h)
author: windows-sdk-content
description: Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.
old-location: com\icontinuecallback.htm
tech.root: com
ms.assetid: 55c960be-48e3-42e1-b459-49227be62171
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContinueCallback, IContinueCallback interface [COM], IContinueCallback interface [COM],described, _com_icontinuecallback, com.icontinuecallback, docobj/IContinueCallback
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContinueCallback interface


## -description


Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.

The <a href="https://msdn.microsoft.com/c84899df-fef1-473d-8278-d715a8ab8ee5">FContinue</a> method is a generic continuation request. <a href="https://msdn.microsoft.com/9031809a-8e5b-48d9-8af9-4a1a07532406">FContinuePrinting</a> carries extra information pertaining to a printing process and is used in the context of <a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContinueCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IContinueCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c84899df-fef1-473d-8278-d715a8ab8ee5">FContinue</a>
</td>
<td align="left" width="63%">
Indicates whether a generic operation should continue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9031809a-8e5b-48d9-8af9-4a1a07532406">FContinuePrinting</a>
</td>
<td align="left" width="63%">
Indicates whether a lengthy printing operation should continue.

</td>
</tr>
</table> 

