---
UID: NF:dsadmin.IDsAdminNewObjPrimarySite.Commit
title: IDsAdminNewObjPrimarySite::Commit (dsadmin.h)
description: The IDsAdminNewObjPrimarySite::Commit method causes a single-page primary object creation extension's IDsAdminNewObjExt::WriteData method to be called and writes the temporary object to persistent memory.
helpviewer_keywords: ["Commit","Commit method [Active Directory]","Commit method [Active Directory]","IDsAdminNewObjPrimarySite interface","IDsAdminNewObjPrimarySite interface [Active Directory]","Commit method","IDsAdminNewObjPrimarySite.Commit","IDsAdminNewObjPrimarySite::Commit","_glines_idsadminnewobjprimarysite_commit","ad.idsadminnewobjprimarysite__commit","ad.idsadminnewobjprimarysite_commit","dsadmin/IDsAdminNewObjPrimarySite::Commit"]
old-location: ad\idsadminnewobjprimarysite_commit.htm
tech.root: ad
ms.assetid: a7e56a9b-bd3c-4229-9735-32ec9549856d
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Active Directory], Commit method [Active Directory],IDsAdminNewObjPrimarySite interface, IDsAdminNewObjPrimarySite interface [Active Directory],Commit method, IDsAdminNewObjPrimarySite.Commit, IDsAdminNewObjPrimarySite::Commit, _glines_idsadminnewobjprimarysite_commit, ad.idsadminnewobjprimarysite__commit, ad.idsadminnewobjprimarysite_commit, dsadmin/IDsAdminNewObjPrimarySite::Commit
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
 - IDsAdminNewObjPrimarySite::Commit
 - dsadmin/IDsAdminNewObjPrimarySite::Commit
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
 - IDsAdminNewObjPrimarySite.Commit
---

# IDsAdminNewObjPrimarySite::Commit


## -description

The <b>IDsAdminNewObjPrimarySite::Commit</b> method causes a single-page primary object creation extension's <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-writedata">IDsAdminNewObjExt::WriteData</a> method to be called and writes the temporary object to persistent memory.



## -returns

Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise. This method fails if the calling extension is not a primary object creation extension. This method also fails if the object creation wizard contains more than one page.

## -remarks

The <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjprimarysite-createnew">IDsAdminNewObjPrimarySite::CreateNew</a> method must be called before <b>IDsAdminNewObjPrimarySite::Commit</b> is called.

When an object creation wizard contains more than one page, the system implements a "Finish" page that displays a summary of the object data to be saved. The system-implemented "Finish" page will perform the  <b>IDsAdminNewObjPrimarySite::Commit</b> operation. If, however, the object creation wizard only contains one page, the  page will have <b>OK</b> and <b>Cancel</b> command buttons instead of the  <b>Back</b>, <b>Next</b> and <b>Cancel</b> buttons normally found in a wizard and no "Finish" page is provided. Because of this, a single-page object creation extension wizard must call <b>Commit</b>.

## -see-also

<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-writedata">IDsAdminNewObjExt::WriteData</a>



<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjprimarysite-createnew">IDsAdminNewObjPrimarySite::CreateNew</a>
