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

# WriteClassStg function


## -description


The <b>WriteClassStg</b> function stores the specified class identifier (CLSID) in a storage object.


## -parameters




### -param pStg [in]


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage object that gets a new CLSID.


### -param rclsid [in]

Pointer to the CLSID to be stored with the object.


## -returns



This function returns HRESULT.




## -remarks



The 
<b>WriteClassStg</b> function writes a CLSID to the specified storage object so that it can be read by the 
<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a> function. Container applications typically call this function before calling the 
<a href="_com_ipersiststorage_save">IPersistStorage::Save</a> method.




## -see-also




<a href="_ole_olesave">OleSave</a>



<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a>
 

 

