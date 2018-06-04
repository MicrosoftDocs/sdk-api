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

# CryptCATEnumerateAttr function


## -description


<p class="CCE_Message">[The <b>CryptCATEnumerateAttr</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateAttr</b> function enumerates the attributes associated with  a member of a catalog. This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatalog [in]

Handle for the catalog that contains the member identified by <i>pCatMember</i>. This value cannot be <b>NULL</b>.


### -param pCatMember [in]

A pointer to the <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that identifies which member of the catalog is being enumerated.


### -param pPrevAttr [in]

A pointer to the previously returned value from this function or pointer to <b>NULL</b> to start the enumeration.


## -returns



The return value is a pointer to the  CRYPTCATATTRIBUTE structure that contains the attribute information or <b>NULL</b>, if no more attributes are in the enumeration or if an error is encountered. The returned pointer is passed in as the <i>pPrevAttr</i> parameter for subsequent calls to this function.




## -remarks



Do not free the returned pointer nor any of the members pointed to by the returned pointer. 




## -see-also




<a href="https://msdn.microsoft.com/57b6ff5c-e47e-41ac-8ec8-01a47ea77acf">CryptCATEnumerateCatAttr</a>
 

 

