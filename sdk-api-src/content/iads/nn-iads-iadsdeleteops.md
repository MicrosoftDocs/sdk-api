---
UID: NN:iads.IADsDeleteOps
title: IADsDeleteOps (iads.h)
description: The IADsDeleteOps interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.
old-location: adsi\iadsdeleteops.htm
tech.root: adsi
ms.assetid: 329d7061-9aa2-4f4e-a0ec-a0cbb1d231f5
ms.date: 12/05/2018
ms.keywords: IADsDeleteOps, IADsDeleteOps interface [ADSI], IADsDeleteOps interface [ADSI],described, _ds_iadsdeleteops, adsi.iadsdeleteops, iads/IADsDeleteOps
f1_keywords:
- iads/IADsDeleteOps
dev_langs:
- c++
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IADsDeleteOps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsDeleteOps interface


## -description


The <b>IADsDeleteOps</b> interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.

The interface is designed to offer features that complement  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>. To remove an object from the directory store, request its parent object to perform the operation. That amounts to calling the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscontainer-delete">IADsContainer::Delete</a> method on the contained object. When the object also implements the <b>IADsDeleteOps</b> interface, you can instruct the object to remove itself, and all the contained objects, by calling the <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a> method directly on the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsDeleteOps</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsDeleteOps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsDeleteOps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">DeleteObject</a>
</td>
<td align="left" width="63%">
Deletes the object from the directory.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/access-control-and-object-deletion">Access Control and Object Deletion</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadscontainer-delete">IADsContainer::Delete</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadsdeleteops-interface">IADsDeleteOps Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

