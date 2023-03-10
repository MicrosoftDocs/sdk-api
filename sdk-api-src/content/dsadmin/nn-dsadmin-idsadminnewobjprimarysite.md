---
UID: NN:dsadmin.IDsAdminNewObjPrimarySite
title: IDsAdminNewObjPrimarySite (dsadmin.h)
description: The IDsAdminNewObjPrimarySite interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory.
helpviewer_keywords: ["IDsAdminNewObjPrimarySite","IDsAdminNewObjPrimarySite interface [Active Directory]","IDsAdminNewObjPrimarySite interface [Active Directory]","described","_glines_idsadminnewobjprimarysite","ad.idsadminnewobjprimarysite","dsadmin/IDsAdminNewObjPrimarySite"]
old-location: ad\idsadminnewobjprimarysite.htm
tech.root: ad
ms.assetid: cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjPrimarySite, IDsAdminNewObjPrimarySite interface [Active Directory], IDsAdminNewObjPrimarySite interface [Active Directory],described, _glines_idsadminnewobjprimarysite, ad.idsadminnewobjprimarysite, dsadmin/IDsAdminNewObjPrimarySite
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
 - IDsAdminNewObjPrimarySite
 - dsadmin/IDsAdminNewObjPrimarySite
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
 - IDsAdminNewObjPrimarySite
---

# IDsAdminNewObjPrimarySite interface


## -description

The <b>IDsAdminNewObjPrimarySite</b> interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory. To obtain an  instance of this interface call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on the <a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a> interface passed to <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>.

## -inheritance

The <b>IDsAdminNewObjPrimarySite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObjPrimarySite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>
