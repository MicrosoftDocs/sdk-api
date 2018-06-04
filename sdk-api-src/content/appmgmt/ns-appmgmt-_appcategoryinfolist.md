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

# _APPCATEGORYINFOLIST structure


## -description


Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.  


## -struct-fields




### -field cCategory

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that specifies the count of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> elements in the array pointed to by <b>pCategoryInfo</b>.


### -field pCategoryInfo

Type: <b><a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a>*</b>


          A pointer to an array of <a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a> structures. This array contains all the categories an application publisher supports and must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
        


### -field pCategoryInfo.size_is

 


### -field pCategoryInfo.size_is.cCategory

 




## -see-also




<a href="https://msdn.microsoft.com/7a0e61cb-97f8-4ca2-a85a-889e671099d0">APPCATEGORYINFO</a>



<a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>
 

 

