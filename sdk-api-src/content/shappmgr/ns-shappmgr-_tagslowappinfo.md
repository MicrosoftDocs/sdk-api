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

# _tagSlowAppInfo structure


## -description


Provides specialized application information to <b>Add/Remove Programs</b> in Control Panel. This structure is not applicable to published applications.


## -struct-fields




### -field ullSize

Type: <b>ULONGLONG</b>

The size of the application in bytes.


### -field ftLastUsed

Type: <b>FILETIME</b>

The time the application was last used.


### -field iTimesUsed

Type: <b>int</b>

The count of times the application has been used.


### -field pszImage

Type: <b>LPWSTR</b>

A pointer to a string containing the path to the image that represents the application. The string buffer must be allocated using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> and freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/02f8e527-1c3c-4a2e-bf55-4f33c6a7b822">IShellApp::GetSlowAppInfo</a> and <a href="https://msdn.microsoft.com/655edc51-0967-4b94-9eef-da213e735e0a">IShellApp::GetCachedSlowAppInfo</a> interfaces, neither of which are applicable to published applications. Therefore, this structure is also not applicable to published applications.




## -see-also




<a href="https://msdn.microsoft.com/5391444a-53b6-48c9-9a94-d045b3f97182">IAppPublisher</a>
 

 

