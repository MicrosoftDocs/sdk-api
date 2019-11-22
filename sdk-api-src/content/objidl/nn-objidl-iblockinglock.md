---
UID: NN:objidl.IBlockingLock
title: IBlockingLock (objidl.h)

description: Provides a semaphore that can be used to provide temporarily exclusive access to a shared resource such as a file.
old-location: com\iblockinglock.htm
tech.root: com
ms.assetid: 8fccc4f9-17fe-4927-b00d-2815f47857e5

ms.date: 12/05/2018
ms.keywords: IBlockingLock, IBlockingLock interface [COM], IBlockingLock interface [COM],described, _com_iblockinglock, com.iblockinglock, objidl/IBlockingLock
ms.topic: interface
f1_keywords: 
 - "objidl/IBlockingLock"
dev_langs:
 - c++
req.header: objidl.h
req.include-header: 
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
 - ObjIdl.h
api_name:
 - IBlockingLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBlockingLock interface


## -description


Provides a semaphore that can be used to provide temporarily exclusive access to a shared resource such as a file.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBlockingLock</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBlockingLock</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBlockingLock</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iblockinglock-lock">Lock</a>
</td>
<td align="left" width="63%">
Requests a lock on a shared resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-iblockinglock-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Releases a lock on a shared resource.

</td>
</tr>
</table> 

