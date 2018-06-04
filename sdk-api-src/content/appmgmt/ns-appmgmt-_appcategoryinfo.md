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

# _APPCATEGORYINFO structure


## -description


Provides application category information to Add/Remove Programs in Control Panel. The <a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a> structure is used create a complete list of categories for an application publisher.


## -struct-fields




### -field Locale

Type: <b>LCID</b>

Unused.


### -field pszDescription

Type: <b>LPWSTR</b>

A pointer to a string containing the display name of the category. This string displays in the <b>Category</b> list in Add/Remove Programs. This string buffer must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -field AppCategoryId

Type: <b>GUID</b>

A GUID identifying the application category.


## -see-also




<a href="https://msdn.microsoft.com/c590d9ab-ab41-4192-a6c2-c6c2c931e873">APPCATEGORYINFOLIST</a>



<a href="https://msdn.microsoft.com/139a5094-8bb3-4b5d-938d-ba4af5d52d94">IAppPublisher::GetCategories</a>
 

 

