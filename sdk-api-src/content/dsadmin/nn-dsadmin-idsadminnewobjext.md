---
UID: NN:dsadmin.IDsAdminNewObjExt
title: IDsAdminNewObjExt (dsadmin.h)
description: The IDsAdminNewObjExt interface is implemented by an object creation wizard extension.
helpviewer_keywords: ["IDsAdminNewObjExt","IDsAdminNewObjExt interface [Active Directory]","IDsAdminNewObjExt interface [Active Directory]","described","_glines_idsadminnewobjext","ad.idsadminnewobjext","dsadmin/IDsAdminNewObjExt"]
old-location: ad\idsadminnewobjext.htm
tech.root: ad
ms.assetid: a9b98647-b801-4a2a-98a4-d57679c07d55
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjExt, IDsAdminNewObjExt interface [Active Directory], IDsAdminNewObjExt interface [Active Directory],described, _glines_idsadminnewobjext, ad.idsadminnewobjext, dsadmin/IDsAdminNewObjExt
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
 - IDsAdminNewObjExt
 - dsadmin/IDsAdminNewObjExt
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
 - IDsAdminNewObjExt
---

# IDsAdminNewObjExt interface


## -description

The <b>IDsAdminNewObjExt</b> interface is implemented by an object creation wizard extension. This interface is used by the Active Directory administrative MMC snap-ins to control the object creation extension. The snap-in creates an instance of this object by using the CLSID of the extension.

## -inheritance

The <b>IDsAdminNewObjExt</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObjExt</b> also has these types of members:

## -see-also

<a href="/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>
