---
UID: NN:oleidl.IOleCacheControl
title: IOleCacheControl (oleidl.h)
description: Provides proper maintenance of caches. It maintains the caches by connecting the running object's IDataObject implementation to the cache, allowing the cache to receive notifications from the running object.helpviewer_keywords: ["IOleCacheControl","IOleCacheControl interface [COM]","IOleCacheControl interface [COM]","described","_ole_iolecachecontrol","com.iolecachecontrol","oleidl/IOleCacheControl"]
old-location: com\iolecachecontrol.htm
tech.root: com
ms.assetid: 64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a
ms.date: 12/05/2018
ms.keywords: IOleCacheControl, IOleCacheControl interface [COM], IOleCacheControl interface [COM],described, _ole_iolecachecontrol, com.iolecachecontrol, oleidl/IOleCacheControl
f1_keywords:
- oleidl/IOleCacheControl
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OleIdl.h
api_name:
- IOleCacheControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleCacheControl interface


## -description


Provides proper maintenance of caches. It maintains the caches by connecting the running object's <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> implementation to the cache, allowing the cache to receive notifications from the running object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleCacheControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleCacheControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleCacheControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onrun">OnRun</a>
</td>
<td align="left" width="63%">
Notifies the cache that the data source object has entered the running state so that the cache object can establish advise sinks as needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolecachecontrol-onstop">OnStop</a>
</td>
<td align="left" width="63%">
Notifies the cache that it should terminate any existing advise sinks.

</td>
</tr>
</table> 

