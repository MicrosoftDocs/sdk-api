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
 

 

