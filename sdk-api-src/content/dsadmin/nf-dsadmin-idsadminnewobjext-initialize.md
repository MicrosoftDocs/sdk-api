---
UID: NF:dsadmin.IDsAdminNewObjExt.Initialize
title: IDsAdminNewObjExt::Initialize
author: windows-sdk-content
description: The IDsAdminNewObjExt::Initialize method initializes an object creation wizard extension.
old-location: ad\idsadminnewobjext_initialize.htm
old-project: ad
ms.assetid: 38dd4f43-6f8f-460a-9c5d-0a506d993101
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IDsAdminNewObjExt interface [Active Directory],Initialize method, IDsAdminNewObjExt.Initialize, IDsAdminNewObjExt::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_initialize, ad.idsadminnewobjext__initialize, ad.idsadminnewobjext_initialize, dsadmin/IDsAdminNewObjExt::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IDsAdminNewObjExt.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminNewObjExt::Initialize


## -description


The <b>IDsAdminNewObjExt::Initialize</b> method initializes an object creation wizard extension.


## -parameters




### -param pADsContainerObj [in]

Pointer to the <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface of an existing container where the object are created. This parameter must not be <b>NULL</b>. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> or <a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>.


### -param pADsCopySource [in]

Pointer to the <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface of the object from which a copy is made. If the new object is not copied from another object, this parameter is <b>NULL</b>. For more information about copy operations, see the Remarks section. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> or <a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>.


### -param lpszClassName [in]

Pointer to a <b>WCHAR</b> string containing the LDAP name of the object class to be created. This parameter must not be <b>NULL</b>. Supported values are: "user", "computer", "printQueue", "group", and "contact".


### -param pDsAdminNewObj [in]

Pointer to an <a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a> interface that contains additional data about the wizard. You can also obtain the <a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a> interface of the primary extension by calling <a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on this interface. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a> or <b>IUnknown::QueryInterface</b>.


### -param pDispInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/966e2093-6ebd-42a0-923d-17f0494a9d0c">DSA_NEWOBJ_DISPINFO</a> structure that contains additional data about the object creation wizard.


## -returns



Returns <b>S_OK</b> if successful or an OLE-defined error code otherwise.




## -remarks



An object in Active Directory Domain Services can either be created from nothing or copied from an existing object. If the new object is created from an existing object, <i>pADsCopySource</i> will contain a pointer to the object from which the copy is made. If the new object is not being copied from another object, <i>pADsCopySource</i> will be <b>NULL</b>. The copy operation is only supported for user objects.




## -see-also




<a href="https://msdn.microsoft.com/966e2093-6ebd-42a0-923d-17f0494a9d0c">DSA_NEWOBJ_DISPINFO</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a>



<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a>



<a href="https://msdn.microsoft.com/library/ms691379(v=VS.85).aspx">IUnknown::AddRef</a>



<a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>
 

 

