---
UID: NN:dsadmin.IDsAdminNewObj
title: IDsAdminNewObj
author: windows-sdk-content
description: The IDsAdminNewObj interface is used by a primary or secondary object creation wizard extension to obtain page count data and to control the command buttons in the wizard.
old-location: ad\idsadminnewobj.htm
old-project: AD
ms.assetid: b38016a2-bbb7-4715-81cc-bd9911fb5a3b
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: IDsAdminNewObj, IDsAdminNewObj interface [Active Directory], IDsAdminNewObj interface [Active Directory],described, _glines_idsadminnewobj, ad.idsadminnewobj, dsadmin/IDsAdminNewObj
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DSAdmin.dll
api_name:
-	IDsAdminNewObj
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminNewObj interface


## -description


The <b>IDsAdminNewObj</b> interface is used by a primary or secondary  object creation wizard extension to obtain page count data and to control the command buttons in the wizard. An instance of this interface is passed to the extension in the <a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObj</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsAdminNewObj</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/babc5baf-33d6-47e9-a99e-81ed339f71d6">GetPageCounts</a>
</td>
<td align="left" width="63%">
Obtains the total number of pages in the wizard as well as the index of the first page of the  extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cc888f4-b884-4e81-8dec-6f12c35d9ee4">SetButtons</a>
</td>
<td align="left" width="63%">
Enables or disables the "Next" command button in the wizard for a specific page.

</td>
</tr>
</table> 


## -see-also




<a href="ad.admin_interfaes_in_active_directory_domain_services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a>



<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">IDsAdminNewObjExt::Initialize</a>



<a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a>
 

 

