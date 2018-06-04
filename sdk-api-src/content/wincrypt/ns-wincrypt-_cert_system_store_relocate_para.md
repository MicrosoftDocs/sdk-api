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

# _CERT_SYSTEM_STORE_RELOCATE_PARA structure


## -description


The <b>CERT_SYSTEM_STORE_RELOCATE_PARA</b> structure contains data to be passed to 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> when that function's <i>dwFlags</i> parameter is set to CERT_SYSTEM_STORE_RELOCATE_FLAG. It allows the application to specify not only the name of the store to be opened, but also registry hKey information indicating a registry location other than the default location.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hKeyBase

A handle to registry hKey.


### -field DUMMYUNIONNAME.pvBase

A pointer to a void to allow the system store location's base to be passed in a number of different forms.


### -field DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME2.pvSystemStore

A pointer to a void to allow the name of the system store to be passed in various forms.


### -field DUMMYUNIONNAME2.pszSystemStore

A null-terminated <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string that names the system store.


### -field DUMMYUNIONNAME2.pwszSystemStore

A null-terminated Unicode string that names the system store.


## -remarks



The relocate capability is used to access system stores persisted in the Group Policy Template (GPT). For example, the Group Policy Editor's MMC snap-in extension for managing group policy trust lists and certificates uses the GPT's base HKEY to call 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>.




## -see-also




<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>
 

 

