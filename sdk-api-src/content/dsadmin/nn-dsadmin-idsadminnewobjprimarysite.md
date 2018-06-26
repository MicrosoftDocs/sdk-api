---
UID: NN:dsadmin.IDsAdminNewObjPrimarySite
title: IDsAdminNewObjPrimarySite
author: windows-sdk-content
description: The IDsAdminNewObjPrimarySite interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory.
old-location: ad\idsadminnewobjprimarysite.htm
old-project: AD
ms.assetid: cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDsAdminNewObjPrimarySite, IDsAdminNewObjPrimarySite interface [Active Directory], IDsAdminNewObjPrimarySite interface [Active Directory],described, _glines_idsadminnewobjprimarysite, ad.idsadminnewobjprimarysite, dsadmin/IDsAdminNewObjPrimarySite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DRT_ADDRESS_LIST, *PDRT_ADDRESS_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DSAdmin.dll
api_name:
 - IDsAdminNewObjPrimarySite
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminNewObjPrimarySite interface


## -description


The <b>IDsAdminNewObjPrimarySite</b> interface is implemented by the system and is used by a primary object creation extension to create a new temporary object in Active Directory Domain Services and then commit the object to persistent memory. To obtain an  instance of this interface call <a href="_com_iunknown_queryinterface">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on the <a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a> interface passed to <a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObjPrimarySite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsAdminNewObjPrimarySite</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Writes a temporary object to persistent memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec685ae1-6a37-43d3-84ed-7409611ab63b">CreateNew</a>
</td>
<td align="left" width="63%">
Enables a primary object creation extension to create a temporary object.

</td>
</tr>
</table> 


## -see-also




<a href="ad.admin_interfaes_in_active_directory_domain_services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a>



<a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a>
 

 

