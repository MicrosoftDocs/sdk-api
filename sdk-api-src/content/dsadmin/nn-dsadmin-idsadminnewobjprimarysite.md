---
UID: NN:dsadmin.IDsAdminNewObjPrimarySite
title: IDsAdminNewObjPrimarySite (dsadmin.h)
description: The IDsAdminNewObjPrimarySite interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory.helpviewer_keywords: ["IDsAdminNewObjPrimarySite","IDsAdminNewObjPrimarySite interface [Active Directory]","IDsAdminNewObjPrimarySite interface [Active Directory]","described","_glines_idsadminnewobjprimarysite","ad.idsadminnewobjprimarysite","dsadmin/IDsAdminNewObjPrimarySite"]
old-location: ad\idsadminnewobjprimarysite.htm
tech.root: ad
ms.assetid: cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjPrimarySite, IDsAdminNewObjPrimarySite interface [Active Directory], IDsAdminNewObjPrimarySite interface [Active Directory],described, _glines_idsadminnewobjprimarysite, ad.idsadminnewobjprimarysite, dsadmin/IDsAdminNewObjPrimarySite
f1_keywords:
- dsadmin/IDsAdminNewObjPrimarySite
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DSAdmin.dll
api_name:
- IDsAdminNewObjPrimarySite
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminNewObjPrimarySite interface


## -description


The <b>IDsAdminNewObjPrimarySite</b> interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory. To obtain an  instance of this interface call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on the <a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a> interface passed to <a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObjPrimarySite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObjPrimarySite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsAdminNewObjPrimarySite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjprimarysite-commit">Commit</a>
</td>
<td align="left" width="63%">
Writes a temporary object to persistent memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjprimarysite-createnew">CreateNew</a>
</td>
<td align="left" width="63%">
Enables a primary object creation extension to create a temporary object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>
 

 

