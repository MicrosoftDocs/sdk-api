---
UID: NF:dsadmin.IDsAdminNewObjExt.SetObject
title: IDsAdminNewObjExt::SetObject (dsadmin.h)
description: The IDsAdminNewObjExt::SetObject method provides the object creation extension with a pointer to the directory object created.
helpviewer_keywords: ["IDsAdminNewObjExt interface [Active Directory]","SetObject method","IDsAdminNewObjExt.SetObject","IDsAdminNewObjExt::SetObject","SetObject","SetObject method [Active Directory]","SetObject method [Active Directory]","IDsAdminNewObjExt interface","_glines_idsadminnewobjext_setobject","ad.idsadminnewobjext__setobject","ad.idsadminnewobjext_setobject","dsadmin/IDsAdminNewObjExt::SetObject"]
old-location: ad\idsadminnewobjext_setobject.htm
tech.root: ad
ms.assetid: e6dbb0ed-e20e-49c7-8247-d5688be93d8e
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjExt interface [Active Directory],SetObject method, IDsAdminNewObjExt.SetObject, IDsAdminNewObjExt::SetObject, SetObject, SetObject method [Active Directory], SetObject method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_setobject, ad.idsadminnewobjext__setobject, ad.idsadminnewobjext_setobject, dsadmin/IDsAdminNewObjExt::SetObject
req.header: dsadmin.h
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
req.dll: DSAdmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsAdminNewObjExt::SetObject
 - dsadmin/IDsAdminNewObjExt::SetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObjExt.SetObject
---

# IDsAdminNewObjExt::SetObject


## -description

The <b>IDsAdminNewObjExt::SetObject</b> method provides the object creation extension with a pointer to the directory object created.

## -parameters

### -param pADsObj [in]

Pointer to an <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface for the object. This parameter may be <b>NULL</b>. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> or <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

## -returns

The method should always return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>