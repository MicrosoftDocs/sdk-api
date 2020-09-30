---
UID: NF:dsadmin.IDsAdminNewObjExt.GetSummaryInfo
title: IDsAdminNewObjExt::GetSummaryInfo (dsadmin.h)
description: The IDsAdminNewObjExt::GetSummaryInfo method obtains a string that contains a summary of the data gathered by the new object wizard extension page. This string is displayed in the wizard Finish page.
helpviewer_keywords: ["GetSummaryInfo","GetSummaryInfo method [Active Directory]","GetSummaryInfo method [Active Directory]","IDsAdminNewObjExt interface","IDsAdminNewObjExt interface [Active Directory]","GetSummaryInfo method","IDsAdminNewObjExt.GetSummaryInfo","IDsAdminNewObjExt::GetSummaryInfo","_glines_idsadminnewobjext_getsummaryinfo","ad.idsadminnewobjext__getsummaryinfo","ad.idsadminnewobjext_getsummaryinfo","dsadmin/IDsAdminNewObjExt::GetSummaryInfo"]
old-location: ad\idsadminnewobjext_getsummaryinfo.htm
tech.root: ad
ms.assetid: 61d97253-360a-4e35-a05a-33315d153c0f
ms.date: 12/05/2018
ms.keywords: GetSummaryInfo, GetSummaryInfo method [Active Directory], GetSummaryInfo method [Active Directory],IDsAdminNewObjExt interface, IDsAdminNewObjExt interface [Active Directory],GetSummaryInfo method, IDsAdminNewObjExt.GetSummaryInfo, IDsAdminNewObjExt::GetSummaryInfo, _glines_idsadminnewobjext_getsummaryinfo, ad.idsadminnewobjext__getsummaryinfo, ad.idsadminnewobjext_getsummaryinfo, dsadmin/IDsAdminNewObjExt::GetSummaryInfo
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
 - IDsAdminNewObjExt::GetSummaryInfo
 - dsadmin/IDsAdminNewObjExt::GetSummaryInfo
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
 - IDsAdminNewObjExt.GetSummaryInfo
---

# IDsAdminNewObjExt::GetSummaryInfo


## -description

The <b>IDsAdminNewObjExt::GetSummaryInfo</b> method obtains a string that contains a summary of the data gathered by the new object wizard extension page. This string is displayed in the wizard Finish page.

## -parameters

### -param pBstrText [out]

A pointer to a <b>BSTR</b> value that receives the summary text. To allocate this value, call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The caller must free this memory by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

## -returns

If the method is successful, <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned. If the extension does not provide a summary string, this method should return <b>E_NOTIMPL</b>.

## -remarks

Support of this method is optional. If the extension does not supply summary information, it should return <b>E_NOTIMPL</b> from this method.

## -see-also

<a href="/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>