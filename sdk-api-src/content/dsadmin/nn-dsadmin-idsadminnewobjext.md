---
UID: NN:dsadmin.IDsAdminNewObjExt
title: IDsAdminNewObjExt
author: windows-sdk-content
description: The IDsAdminNewObjExt interface is implemented by an object creation wizard extension.
old-location: ad\idsadminnewobjext.htm
tech.root: AD
ms.assetid: a9b98647-b801-4a2a-98a4-d57679c07d55
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDsAdminNewObjExt, IDsAdminNewObjExt interface [Active Directory], IDsAdminNewObjExt interface [Active Directory],described, _glines_idsadminnewobjext, ad.idsadminnewobjext, dsadmin/IDsAdminNewObjExt
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNewObjExt interface


## -description


The <b>IDsAdminNewObjExt</b> interface is implemented by an object creation wizard extension. This interface is used by the Active Directory administrative MMC snap-ins to control the object creation extension. The snap-in creates an instance of this object by using the CLSID of the extension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDsAdminNewObjExt</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDsAdminNewObjExt</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4e16385f-b38a-4961-95ec-c81fd538ae2b">AddPages</a>
</td>
<td align="left" width="63%">
Called to enable the object creation wizard extension to add the desired  pages to the wizard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61d97253-360a-4e35-a05a-33315d153c0f">GetSummaryInfo</a>
</td>
<td align="left" width="63%">
Obtains a string that contains a summary of the data gathered by the new object wizard extension page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38dd4f43-6f8f-460a-9c5d-0a506d993101">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object creation wizard extension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1bb1eb6-db96-4322-8beb-0b9a3c6b0318">OnError</a>
</td>
<td align="left" width="63%">
Called when an error occurs in the wizard pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">SetObject</a>
</td>
<td align="left" width="63%">
Provides the object creation extension with a pointer to the  object created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1788c124-c740-4f77-9687-63113d3b14a8">WriteData</a>
</td>
<td align="left" width="63%">
Enables the object creation wizard extension to write its data into the object.

</td>
</tr>
</table> 


## -see-also




<a href="ad.admin_interfaes_in_active_directory_domain_services">Admin Interfaces in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a>



<a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a>



<a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a>
 

 

