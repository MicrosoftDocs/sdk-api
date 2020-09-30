---
UID: NN:objidl.ISynchronizeHandle
title: ISynchronizeHandle (objidl.h)
description: Retrieves a handle associated with a synchronization object.
helpviewer_keywords: ["ISynchronizeHandle","ISynchronizeHandle interface [COM]","ISynchronizeHandle interface [COM]","described","_com_isynchronizehandle","com.isynchronizehandle","objidlbase/ISynchronizeHandle"]
old-location: com\isynchronizehandle.htm
tech.root: com
ms.assetid: 93b2e682-78da-4a61-a045-8d71b3834e1d
ms.date: 12/05/2018
ms.keywords: ISynchronizeHandle, ISynchronizeHandle interface [COM], ISynchronizeHandle interface [COM],described, _com_isynchronizehandle, com.isynchronizehandle, objidlbase/ISynchronizeHandle
req.header: objidl.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISynchronizeHandle
 - objidl/ISynchronizeHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - ISynchronizeHandle
---

# ISynchronizeHandle interface


## -description

Retrieves a handle associated with a synchronization object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronizeHandle</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISynchronizeHandle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronizeHandle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/objidl/nf-objidl-isynchronizehandle-gethandle">GetHandle</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the synchronization object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isynchronizeevent">ISynchronizeEvent</a>