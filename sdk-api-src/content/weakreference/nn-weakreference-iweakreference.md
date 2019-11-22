---
UID: NN:weakreference.IWeakReference
title: IWeakReference (weakreference.h)

description: Represents a weak reference to an object.
old-location: winrt\iweakreference.htm
tech.root: WinRT
ms.assetid: fae8bf21-2a38-4e98-9a11-89c548da9e95

ms.date: 12/05/2018
ms.keywords: IWeakReference, IWeakReference interface [Windows Runtime], IWeakReference interface [Windows Runtime],described, weakreference/IWeakReference, winrt.iweakreference
ms.topic: interface
f1_keywords: 
 - "weakreference/IWeakReference"
dev_langs:
 - c++
req.header: weakreference.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WeakReference.idl
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
 - WeakReference.h
api_name:
 - IWeakReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWeakReference interface


## -description


Represents a weak reference to an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWeakReference</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWeakReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWeakReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/weakreference/nf-weakreference-iweakreference-resolve(refiid_iinspectable)">Resolve</a>
</td>
<td align="left" width="63%">
Resolves a weak reference by returning a strong reference to the specified object.

</td>
</tr>
</table> 

