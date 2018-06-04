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

# ISdoDictionaryOld::GetAttributeInfo


## -description


The <b>GetAttributeInfo</b> 
    retrieves information for the specified attribute.


## -parameters




### -param Id [in]

Specifies the ID for the attribute.


### -param pInfoIDs [in]

Pointer to an array of information IDs. This pointer cannot be <b>NULL</b>.


### -param pInfoValues [out]

Pointer to a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> of 
      information values.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



Although Server Data Objects (SDO) exposes this method, you do not need it in order to use SDO. The use of 
    this method is discouraged.




## -see-also




<a href="https://msdn.microsoft.com/84ed435c-c6e8-41e7-9a5f-acd78fce4a10">ATTRIBUTEINFO</a>



<a href="https://msdn.microsoft.com/5aaa4008-3b39-4d1d-90db-79631e5bb6b9">ISdoDictionaryOld</a>



<a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

