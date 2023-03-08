---
UID: NN:dsadmin.IDsAdminNewObj
title: IDsAdminNewObj (dsadmin.h)
description: The IDsAdminNewObj interface is used by a primary or secondary object creation wizard extension to obtain page count data and to control the command buttons in the wizard.
helpviewer_keywords: ["IDsAdminNewObj","IDsAdminNewObj interface [Active Directory]","IDsAdminNewObj interface [Active Directory]","described","_glines_idsadminnewobj","ad.idsadminnewobj","dsadmin/IDsAdminNewObj"]
old-location: ad\idsadminnewobj.htm
tech.root: ad
ms.assetid: b38016a2-bbb7-4715-81cc-bd9911fb5a3b
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObj, IDsAdminNewObj interface [Active Directory], IDsAdminNewObj interface [Active Directory],described, _glines_idsadminnewobj, ad.idsadminnewobj, dsadmin/IDsAdminNewObj
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
 - IDsAdminNewObj
 - dsadmin/IDsAdminNewObj
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
 - IDsAdminNewObj
---

# IDsAdminNewObj interface


## -description

The <b>IDsAdminNewObj</b> interface is used by a primary or secondary  object creation wizard extension to obtain page count data and to control the command buttons in the wizard. An instance of this interface is passed to the extension in the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a> method.

## -inheritance

The <b>IDsAdminNewObj</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObj</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>
