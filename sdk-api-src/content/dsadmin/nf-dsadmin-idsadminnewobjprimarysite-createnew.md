---
UID: NF:dsadmin.IDsAdminNewObjPrimarySite.CreateNew
title: IDsAdminNewObjPrimarySite::CreateNew (dsadmin.h)
description: The IDsAdminNewObjPrimarySite::CreateNew method enables a primary object creation extension to create a temporary directory service object in Active Directory Domain Services.
helpviewer_keywords: ["CreateNew","CreateNew method [Active Directory]","CreateNew method [Active Directory]","IDsAdminNewObjPrimarySite interface","IDsAdminNewObjPrimarySite interface [Active Directory]","CreateNew method","IDsAdminNewObjPrimarySite.CreateNew","IDsAdminNewObjPrimarySite::CreateNew","_glines_idsadminnewobjprimarysite_createnew","ad.idsadminnewobjprimarysite__createnew","ad.idsadminnewobjprimarysite_createnew","dsadmin/IDsAdminNewObjPrimarySite::CreateNew"]
old-location: ad\idsadminnewobjprimarysite_createnew.htm
tech.root: ad
ms.assetid: ec685ae1-6a37-43d3-84ed-7409611ab63b
ms.date: 12/05/2018
ms.keywords: CreateNew, CreateNew method [Active Directory], CreateNew method [Active Directory],IDsAdminNewObjPrimarySite interface, IDsAdminNewObjPrimarySite interface [Active Directory],CreateNew method, IDsAdminNewObjPrimarySite.CreateNew, IDsAdminNewObjPrimarySite::CreateNew, _glines_idsadminnewobjprimarysite_createnew, ad.idsadminnewobjprimarysite__createnew, ad.idsadminnewobjprimarysite_createnew, dsadmin/IDsAdminNewObjPrimarySite::CreateNew
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
 - IDsAdminNewObjPrimarySite::CreateNew
 - dsadmin/IDsAdminNewObjPrimarySite::CreateNew
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
 - IDsAdminNewObjPrimarySite.CreateNew
---

# IDsAdminNewObjPrimarySite::CreateNew


## -description

The <b>IDsAdminNewObjPrimarySite::CreateNew</b> method enables a primary object creation extension to create a temporary directory service object in Active Directory Domain Services. This object is then passed to each object creation extension in the extension's <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a> method.

## -parameters

### -param pszName [in]

Pointer to a <b>WCHAR</b> string that contains the name of the object to be created.

## -returns

If the  method 
      succeeds, <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned. This method fails if the calling extension is not a primary object creation extension.

## -see-also

<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>