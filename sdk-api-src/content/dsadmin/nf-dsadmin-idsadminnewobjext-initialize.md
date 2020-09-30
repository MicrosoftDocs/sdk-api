---
UID: NF:dsadmin.IDsAdminNewObjExt.Initialize
title: IDsAdminNewObjExt::Initialize (dsadmin.h)
description: The IDsAdminNewObjExt::Initialize method initializes an object creation wizard extension.
helpviewer_keywords: ["IDsAdminNewObjExt interface [Active Directory]","Initialize method","IDsAdminNewObjExt.Initialize","IDsAdminNewObjExt::Initialize","Initialize","Initialize method [Active Directory]","Initialize method [Active Directory]","IDsAdminNewObjExt interface","_glines_idsadminnewobjext_initialize","ad.idsadminnewobjext__initialize","ad.idsadminnewobjext_initialize","dsadmin/IDsAdminNewObjExt::Initialize"]
old-location: ad\idsadminnewobjext_initialize.htm
tech.root: ad
ms.assetid: 38dd4f43-6f8f-460a-9c5d-0a506d993101
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjExt interface [Active Directory],Initialize method, IDsAdminNewObjExt.Initialize, IDsAdminNewObjExt::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_initialize, ad.idsadminnewobjext__initialize, ad.idsadminnewobjext_initialize, dsadmin/IDsAdminNewObjExt::Initialize
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
 - IDsAdminNewObjExt::Initialize
 - dsadmin/IDsAdminNewObjExt::Initialize
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
 - IDsAdminNewObjExt.Initialize
---

# IDsAdminNewObjExt::Initialize


## -description

The <b>IDsAdminNewObjExt::Initialize</b> method initializes an object creation wizard extension.

## -parameters

### -param pADsContainerObj [in]

Pointer to the <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface of an existing container where the object are created. This parameter must not be <b>NULL</b>. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> or <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

### -param pADsCopySource [in]

Pointer to the <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a> interface of the object from which a copy is made. If the new object is not copied from another object, this parameter is <b>NULL</b>. For more information about copy operations, see the Remarks section. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> or <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.

### -param lpszClassName [in]

Pointer to a <b>WCHAR</b> string containing the LDAP name of the object class to be created. This parameter must not be <b>NULL</b>. Supported values are: "user", "computer", "printQueue", "group", and "contact".

### -param pDsAdminNewObj [in]

Pointer to an <a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a> interface that contains additional data about the wizard. You can also obtain the <a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a> interface of the primary extension by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on this interface. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> or <b>IUnknown::QueryInterface</b>.

### -param pDispInfo [in]

Pointer to a <a href="/windows/desktop/api/dsadmin/ns-dsadmin-dsa_newobj_dispinfo">DSA_NEWOBJ_DISPINFO</a> structure that contains additional data about the object creation wizard.

## -returns

Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise.

## -remarks

An object in Active Directory Domain Services can either be created from nothing or copied from an existing object. If the new object is created from an existing object, <i>pADsCopySource</i> will contain a pointer to the object from which the copy is made. If the new object is not being copied from another object, <i>pADsCopySource</i> will be <b>NULL</b>. The copy operation is only supported for user objects.

## -see-also

<a href="/windows/desktop/api/dsadmin/ns-dsadmin-dsa_newobj_dispinfo">DSA_NEWOBJ_DISPINFO</a>



<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>



<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>