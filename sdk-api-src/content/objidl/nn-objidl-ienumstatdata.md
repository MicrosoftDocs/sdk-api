---
UID: NN:objidl.IEnumSTATDATA
title: IEnumSTATDATA (objidl.h)
description: Enumerates the advisory connection information for a data object.
helpviewer_keywords: ["IEnumSTATDATA","IEnumSTATDATA interface [COM]","IEnumSTATDATA interface [COM]","described","_ole_ienumstatdata","com.ienumstatdata","objidl/IEnumSTATDATA"]
old-location: com\ienumstatdata.htm
tech.root: com
ms.assetid: 8e2f6655-4a09-4868-a909-18999104b3ff
ms.date: 12/05/2018
ms.keywords: IEnumSTATDATA, IEnumSTATDATA interface [COM], IEnumSTATDATA interface [COM],described, _ole_ienumstatdata, com.ienumstatdata, objidl/IEnumSTATDATA
f1_keywords:
- objidl/IEnumSTATDATA
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
- IEnumSTATDATA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATDATA interface


## -description


Enumerates the advisory connection information for a data object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATDATA</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATDATA</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATDATA</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatdata-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatdata-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatdata-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatdata-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataadviseholder-enumadvise">IDataAdviseHolder::EnumAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-enumdadvise">IDataObject::EnumDAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolecache-enumcache">IOleCache::EnumCache</a>
 

 

