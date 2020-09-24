---
UID: NN:oleidl.IOleContainer
title: IOleContainer (oleidl.h)
description: Enumerates objects in a compound document or lock a container in the running state. Container and object applications both implement this interface.
helpviewer_keywords: ["IOleContainer","IOleContainer interface [COM]","IOleContainer interface [COM]","described","_ole_iolecontainer","com.iolecontainer","oleidl/IOleContainer"]
old-location: com\iolecontainer.htm
tech.root: com
ms.assetid: 98549309-8ac8-4391-92ab-8a62269ff579
ms.date: 12/05/2018
ms.keywords: IOleContainer, IOleContainer interface [COM], IOleContainer interface [COM],described, _ole_iolecontainer, com.iolecontainer, oleidl/IOleContainer
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleContainer
 - oleidl/IOleContainer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleContainer
---

# IOleContainer interface


## -description

Enumerates objects in a compound document or lock a container in the running state. Container and object applications both implement this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleContainer</b> interface inherits from <a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>. <b>IOleContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-enumobjects">EnumObjects</a>
</td>
<td align="left" width="63%">
Enumerates the objects in the current container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecontainer-lockcontainer">LockContainer</a>
</td>
<td align="left" width="63%">
Keeps the container for embedded objects running until explicitly released.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iparsedisplayname">IParseDisplayName</a>