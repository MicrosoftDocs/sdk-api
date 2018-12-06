---
UID: NF:dsadmin.IDsAdminNewObjExt.SetObject
title: IDsAdminNewObjExt::SetObject
author: windows-sdk-content
description: The IDsAdminNewObjExt::SetObject method provides the object creation extension with a pointer to the directory object created.
old-location: ad\idsadminnewobjext_setobject.htm
tech.root: ad
ms.assetid: e6dbb0ed-e20e-49c7-8247-d5688be93d8e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDsAdminNewObjExt interface [Active Directory],SetObject method, IDsAdminNewObjExt.SetObject, IDsAdminNewObjExt::SetObject, SetObject, SetObject method [Active Directory], SetObject method [Active Directory],IDsAdminNewObjExt interface, _glines_idsadminnewobjext_setobject, ad.idsadminnewobjext__setobject, ad.idsadminnewobjext_setobject, dsadmin/IDsAdminNewObjExt::SetObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDsAdminNewObjExt.SetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsAdminNewObjExt::SetObject


## -description


The <b>IDsAdminNewObjExt::SetObject</b> method provides the object creation extension with a pointer to the directory object created.


## -parameters




### -param pADsObj [in]

Pointer to an <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface for the object. This parameter may be <b>NULL</b>. If this object is to be kept beyond the scope of this method, the reference count must be incremented by calling <a href="_com_iunknown_addref">IUnknown::AddRef</a> or <a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a>.


## -returns



The method should always return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/a9b98647-b801-4a2a-98a4-d57679c07d55">IDsAdminNewObjExt</a>



<a href="_com_iunknown_addref">IUnknown::AddRef</a>



<a href="_com_iunknown_queryinterface">IUnknown::QueryInterface</a>
 

 

