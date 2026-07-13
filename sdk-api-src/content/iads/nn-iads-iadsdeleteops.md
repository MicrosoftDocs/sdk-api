---
UID: NN:iads.IADsDeleteOps
title: IADsDeleteOps (iads.h)
description: The IADsDeleteOps interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.
helpviewer_keywords: ["IADsDeleteOps","IADsDeleteOps interface [ADSI]","IADsDeleteOps interface [ADSI]","described","_ds_iadsdeleteops","adsi.iadsdeleteops","iads/IADsDeleteOps"]
old-location: adsi\iadsdeleteops.htm
tech.root: adsi
ms.assetid: 329d7061-9aa2-4f4e-a0ec-a0cbb1d231f5
ms.date: 12/05/2018
ms.keywords: IADsDeleteOps, IADsDeleteOps interface [ADSI], IADsDeleteOps interface [ADSI],described, _ds_iadsdeleteops, adsi.iadsdeleteops, iads/IADsDeleteOps
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsDeleteOps
 - iads/IADsDeleteOps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsDeleteOps
---

# IADsDeleteOps interface


## -description

The <b>IADsDeleteOps</b> interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.

The interface is designed to offer features that complement  <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>. To remove an object from the directory store, request its parent object to perform the operation. That amounts to calling the  <a href="/windows/desktop/api/iads/nf-iads-iadscontainer-delete">IADsContainer::Delete</a> method on the contained object. When the object also implements the <b>IADsDeleteOps</b> interface, you can instruct the object to remove itself, and all the contained objects, by calling the <a href="/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a> method directly on the object.

## -inheritance

The <b>IADsDeleteOps</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsDeleteOps</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/access-control-and-object-deletion">Access Control and Object Deletion</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-delete">IADsContainer::Delete</a>



<a href="/windows/desktop/ADSI/iadsdeleteops-interface">IADsDeleteOps Interface</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
