---
UID: NN:comadmin.ICatalogObject
title: ICatalogObject (comadmin.h)
description: Represents items in collections on the COM+ catalog. ICatalogObject enables you to get and put properties exposed by objects in the catalog.
helpviewer_keywords: ["ICatalogObject","ICatalogObject interface [COM+]","ICatalogObject interface [COM+]","described","_cos_ICatalogObject_Interface","comadmin/ICatalogObject","cos.icatalogobject"]
old-location: cos\icatalogobject.htm
tech.root: cos
ms.assetid: fe3f7452-57b2-4f9e-9b48-5dedfe519ac1
ms.date: 12/05/2018
ms.keywords: ICatalogObject, ICatalogObject interface [COM+], ICatalogObject interface [COM+],described, _cos_ICatalogObject_Interface, comadmin/ICatalogObject, cos.icatalogobject
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
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
 - ICatalogObject
 - comadmin/ICatalogObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICatalogObject
---

# ICatalogObject interface


## -description

Represents items in collections on the COM+ catalog. <b>ICatalogObject</b> enables you to get and put properties exposed by objects in the catalog.

The <a href="/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_item">ICatalogCollection::Item</a> method returns a pointer to <b>ICatalogObject</b> when it retrieves an item in the collection.

## -inheritance

The <b>ICatalogObject</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICatalogObject</b> also has these types of members:

