---
UID: NN:dsadmin.IDsAdminNewObjExt
title: IDsAdminNewObjExt (dsadmin.h)
description: The IDsAdminNewObjExt interface is implemented by an object creation wizard extension.helpviewer_keywords: ["IDsAdminNewObjExt","IDsAdminNewObjExt interface [Active Directory]","IDsAdminNewObjExt interface [Active Directory]","described","_glines_idsadminnewobjext","ad.idsadminnewobjext","dsadmin/IDsAdminNewObjExt"]
old-location: ad\idsadminnewobjext.htm
tech.root: ad
ms.assetid: a9b98647-b801-4a2a-98a4-d57679c07d55
ms.date: 12/05/2018
ms.keywords: IDsAdminNewObjExt, IDsAdminNewObjExt interface [Active Directory], IDsAdminNewObjExt interface [Active Directory],described, _glines_idsadminnewobjext, ad.idsadminnewobjext, dsadmin/IDsAdminNewObjExt
f1_keywords:
- dsadmin/IDsAdminNewObjExt
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
- IDsAdminNewObjExt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsAdminNewObjExt interface


## -description


The <b>IDsAdminNewObjExt</b> interface is implemented by an object creation wizard extension. This interface is used by the Active Directory administrative MMC snap-ins to control the object creation extension. The snap-in creates an instance of this object by using the CLSID of the extension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObjExt</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsAdminNewObjExt</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDsAdminNewObjExt</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-addpages">AddPages</a>
</td>
<td align="left" width="63%">
Called to enable the object creation wizard extension to add the desired  pages to the wizard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo">GetSummaryInfo</a>
</td>
<td align="left" width="63%">
Obtains a string that contains a summary of the data gathered by the new object wizard extension page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object creation wizard extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-onerror">OnError</a>
</td>
<td align="left" width="63%">
Called when an error occurs in the wizard pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-setobject">SetObject</a>
</td>
<td align="left" width="63%">
Provides the object creation extension with a pointer to the  object created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-writedata">WriteData</a>
</td>
<td align="left" width="63%">
Enables the object creation wizard extension to write its data into the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/admin-interfaces-in-active-directory-domain-services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadmincreateobj">IDsAdminCreateObj</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobj">IDsAdminNewObj</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsadmin/nn-dsadmin-idsadminnewobjprimarysite">IDsAdminNewObjPrimarySite</a>
 

 

