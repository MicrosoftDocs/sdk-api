---
UID: NN:dsadmin.IDsAdminNewObj
title: IDsAdminNewObj (dsadmin.h)
description: The IDsAdminNewObj interface is used by a primary or secondary object creation wizard extension to obtain page count data and to control the command buttons in the wizard.
old-location: ad\idsadminnewobj.htm
tech.root: ad
ms.assetid: b38016a2-bbb7-4715-81cc-bd9911fb5a3b
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObj, IDsAdminNewObj interface [Active Directory], IDsAdminNewObj interface [Active Directory],described, _glines_idsadminnewobj, ad.idsadminnewobj, dsadmin/IDsAdminNewObj
ms.topic: interface
f1_keywords:
- dsadmin/IDsAdminNewObj
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
- IDsAdminNewObj
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminNewObj interface


## -description


The <b>IDsAdminNewObj</b> interface is used by a primary or secondary  object creation wizard extension to obtain page count data and to control the command buttons in the wizard. An instance of this interface is passed to the extension in the <a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObj</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObj</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsAdminNewObj</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobj-getpagecounts">GetPageCounts</a>
</td>
<td align="left" width="63%">
Obtains the total number of pages in the wizard as well as the index of the first page of the  extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobj-setbuttons">SetButtons</a>
</td>
<td align="left" width="63%">
Enables or disables the "Next" command button in the wizard for a specific page.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjext">IDsAdminNewObjExt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>
 

 

