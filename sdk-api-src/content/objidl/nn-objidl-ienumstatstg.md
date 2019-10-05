---
UID: NN:objidl.IEnumSTATSTG
title: IEnumSTATSTG (objidl.h)
author: windows-sdk-content
description: Enumerates an array of STATSTG structures.
old-location: stg\ienumstatstg.htm
tech.root: Stg
ms.assetid: 93b8b14e-94e4-460b-9846-413affad8e4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSTATSTG, IEnumSTATSTG interface [Structured Storage], IEnumSTATSTG interface [Structured Storage],described, _stg_ienumstatstg, objidl/IEnumSTATSTG, stg.ienumstatstg
ms.topic: interface
f1_keywords: 
 - "objidl/IEnumSTATSTG"
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
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATSTG interface


## -description


The 
<b>IEnumSTATSTG</b> interface enumerates an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures. These structures contain statistical data about  open storage, stream, or byte array objects. 
<b>IEnumSTATSTG</b> has the same methods as all enumerator interfaces: <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-next">Next</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-skip">Skip</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-reset">Reset</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-clone">Clone</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATSTG</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSTATSTG</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATSTG</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-next">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ienumstatstg-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-enumelements">IStorage::EnumElements</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a>
 

 

