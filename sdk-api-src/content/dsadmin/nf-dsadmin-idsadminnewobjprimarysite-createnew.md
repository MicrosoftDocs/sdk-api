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

# IDsAdminNewObjPrimarySite::CreateNew


## -description


The <b>IDsAdminNewObjPrimarySite::CreateNew</b> method enables a primary object creation extension to create a temporary directory service object in Active Directory Domain Services. This object is then passed to each object creation extension in the extension's <a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a> method.


## -parameters




### -param pszName [in]

Pointer to a <b>WCHAR</b> string that contains the name of the object to be created.


## -returns



If the  method 
      succeeds, <b>S_OK</b> is returned. If the method fails, an OLE-defined error code is returned. This method fails if the calling extension is not a primary object creation extension.




## -see-also




<a href="https://msdn.microsoft.com/e6dbb0ed-e20e-49c7-8247-d5688be93d8e">IDsAdminNewObjExt::SetObject</a>



<a href="https://msdn.microsoft.com/cb46cb8f-28ae-44d0-b1de-dc6c090f8fc6">IDsAdminNewObjPrimarySite</a>
 

 

