---
UID: NF:dsadmin.IDsAdminNewObj.GetPageCounts
title: IDsAdminNewObj::GetPageCounts (dsadmin.h)
description: The IDsAdminNewObj::GetPageCounts method obtains the total number of pages in the wizard as well as the index of the first page of the extension.
helpviewer_keywords: ["GetPageCounts","GetPageCounts method [Active Directory]","GetPageCounts method [Active Directory]","IDsAdminNewObj interface","IDsAdminNewObj interface [Active Directory]","GetPageCounts method","IDsAdminNewObj.GetPageCounts","IDsAdminNewObj::GetPageCounts","_glines_idsadminnewobj_getpagecounts","ad.idsadminnewobj__getpagecounts","ad.idsadminnewobj_getpagecounts","dsadmin/IDsAdminNewObj::GetPageCounts"]
old-location: ad\idsadminnewobj_getpagecounts.htm
tech.root: ad
ms.assetid: babc5baf-33d6-47e9-a99e-81ed339f71d6
ms.date: 12/05/2018
ms.keywords: GetPageCounts, GetPageCounts method [Active Directory], GetPageCounts method [Active Directory],IDsAdminNewObj interface, IDsAdminNewObj interface [Active Directory],GetPageCounts method, IDsAdminNewObj.GetPageCounts, IDsAdminNewObj::GetPageCounts, _glines_idsadminnewobj_getpagecounts, ad.idsadminnewobj__getpagecounts, ad.idsadminnewobj_getpagecounts, dsadmin/IDsAdminNewObj::GetPageCounts
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
 - IDsAdminNewObj::GetPageCounts
 - dsadmin/IDsAdminNewObj::GetPageCounts
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
 - IDsAdminNewObj.GetPageCounts
---

# IDsAdminNewObj::GetPageCounts


## -description

The <b>IDsAdminNewObj::GetPageCounts</b> method obtains the total number of pages in the wizard as well as the index of the first page of the  extension.

## -parameters

### -param pnTotal [out]

Pointer to a <b>LONG</b> value that receives the total number of pages contained in the wizard.

### -param pnStartIndex [out]

Pointer to a <b>LONG</b> value that receives the zero-based index of the first page of the extension.

## -returns

This method can return one of these values.


Returns one of the following values.

## -remarks

This function will provide results based on the count of pages added using 
<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-addpages">IDsAdminNewObjExt::AddPages</a>. If there are changes to the number of pages because of page manipulations by Win32 APIs, the supplied values may not be accurate. If this method is called in response to the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a> method, the supplied page counts are most likely to be accurate.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-addpages">IDsAdminNewObjExt::AddPages</a>



<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">IDsAdminNewObjExt::SetObject</a>