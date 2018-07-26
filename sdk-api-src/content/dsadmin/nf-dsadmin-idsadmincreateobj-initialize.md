---
UID: NF:dsadmin.IDsAdminCreateObj.Initialize
title: IDsAdminCreateObj::Initialize
author: windows-sdk-content
description: The IDsAdminCreateObj::Initialize method initializes an IDsAdminCreateObj object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object to copy from.
old-location: ad\idsadmincreateobj_initialize.htm
old-project: ad
ms.assetid: 811863e7-25d2-48d0-bf97-61b49a224c98
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IDsAdminCreateObj interface [Active Directory],Initialize method, IDsAdminCreateObj.Initialize, IDsAdminCreateObj::Initialize, Initialize, Initialize method [Active Directory], Initialize method [Active Directory],IDsAdminCreateObj interface, _glines_idsadmincreateobj_initialize, ad.idsadmincreateobj__initialize, ad.idsadmincreateobj_initialize, dsadmin/IDsAdminCreateObj::Initialize
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
 - IDsAdminCreateObj.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: DSAdmin.dll
req.irql: 
---

# IDsAdminCreateObj::Initialize


## -description


The <b>IDsAdminCreateObj::Initialize</b> method initializes an 
<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a> object with data about the container where the object will be created, the class of the object to be created and, possibly, the source object to copy from.


## -parameters




### -param pADsContainerObj [in]

Pointer to an <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface that represents the  container where the object will be created. This parameter must not be <b>NULL</b>.


### -param pADsCopySource [in]

Pointer to the <a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a> interface of the object from which a copy is made. If the new object is not copied from another object, this parameter is <b>NULL</b>. The copy operation is only supported for user objects.


### -param lpszClassName [in]

Pointer to a <b>WCHAR</b> string that contains the LDAP name of the object class to be created. This parameter must not be <b>NULL</b>. Supported values are: "user", "computer", "printQueue", "group" and "contact".


## -returns



If the method succeeds, 
      <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned.




## -remarks



The <b>IDsAdminCreateObj::Initialize</b> method must be called before <a href="https://msdn.microsoft.com/8c157dd8-b569-4171-bd23-b9bce80dbc21">IDsAdminCreateObj::CreateModal</a> can be called.




## -see-also




<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/93673b29-744a-4100-86b7-8a2eec861c47">IDsAdminCreateObj</a>



<a href="https://msdn.microsoft.com/8c157dd8-b569-4171-bd23-b9bce80dbc21">IDsAdminCreateObj::CreateModal</a>
 

 

