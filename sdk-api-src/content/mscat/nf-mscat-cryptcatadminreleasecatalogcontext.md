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

# CryptCATAdminReleaseCatalogContext function


## -description


<p class="CCE_Message">[The <b>CryptCATAdminReleaseCatalogContext</b>  function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATAdminReleaseCatalogContext</b> function releases a handle to a catalog context previously returned by the <a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a> function. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle previously assigned by the  <a href="https://msdn.microsoft.com/693af055-fa93-4526-aa9c-3a659f8ff78f">CryptCATAdminAcquireContext</a> function.


### -param hCatInfo [in]

Handle previously assigned by the <a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a> function or the <a href="https://msdn.microsoft.com/33ab2d01-94ab-4d23-a054-9da0731485d6">CryptCATAdminEnumCatalogFromHash</a> function.


### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.




## -see-also




<a href="https://msdn.microsoft.com/a227597c-a0af-4b86-bd29-03f478aef244">CryptCATAdminAddCatalog</a>
 

 

