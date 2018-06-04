---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDsAdminNewObjExt::Initialize


## -description


The <b>IDsAdminNewObjExt::Initialize</b> method initializes an object creation wizard extension.


## -parameters




### -param pADsContainerObj [in]

Pointer to the <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface of an existing container where the object are created. This parameter must not be <b>NULL</b>. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="_com_iunknown_addref">IUnknown::AddRef</a> or <a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a>.


### -param pADsCopySource [in]

Pointer to the <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface of the object from which a copy is made. If the new object is not copied from another object, this parameter is <b>NULL</b>. For more information about copy operations, see the Remarks section. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="_com_iunknown_addref">IUnknown::AddRef</a> or <a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a>.


### -param lpszClassName [in]

Pointer to a <b>WCHAR</b> string containing the LDAP name of the object class to be created. This parameter must not be <b>NULL</b>. Supported values are: "user", "computer", "printQueue", "group", and "contact".


### -param pDsAdminNewObj [in]

Pointer to an <a href="https://msdn.microsoft.com/b38016a2-bbb7-4715-81cc-bd9911fb5a3b">IDsAdminNewObj</a> interface that contains additional data about the wizard. You can also obtain the <a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a> interface of the primary extension by calling <a href="_com_iunknown_queryinterface">QueryInterface</a> with <b>IID_IDsAdminNewObjPrimarySite</b> on this interface. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="_com_iunknown_addref">IUnknown::AddRef</a> or <b>IUnknown::QueryInterface</b>.


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



<a href="_com_iunknown_addref">IUnknown::AddRef</a>



<a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a>
 

 

