---
UID: NN:objidlbase.ISynchronizeContainer
title: ISynchronizeContainer (objidlbase.h)
author: windows-sdk-content
description: Manages a group of unsignaled synchronization objects.
old-location: com\isynchronizecontainer.htm
tech.root: com
ms.assetid: 6a5be504-b5fa-491c-ba65-74c5de39e263
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISynchronizeContainer, ISynchronizeContainer interface [COM], ISynchronizeContainer interface [COM],described, _com_isynchronizecontainer, com.isynchronizecontainer, objidlbase/ISynchronizeContainer
ms.topic: interface
f1_keywords: 
 - "objidlbase/ISynchronizeContainer"
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - ISynchronizeContainer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISynchronizeContainer interface


## -description


Manages a group of unsignaled synchronization objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronizeContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISynchronizeContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronizeContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronizecontainer-addsynchronize">AddSynchronize</a>
</td>
<td align="left" width="63%">
Adds a synchronization object to the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isynchronizecontainer-waitmultiple">WaitMultiple</a>
</td>
<td align="left" width="63%">
Waits for any synchronization object in the container to be signaled or for a specified timeout period to elapse, whichever comes first.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-isynchronize">ISynchronize</a>
 

 

