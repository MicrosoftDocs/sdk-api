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

# tagLICINFO structure


## -description


Contains parameters that describe the licensing behavior of a class factory that supports licensing. The structure is filled by calling the <a href="https://msdn.microsoft.com/e55d1089-b1df-4de0-9a19-cbd255b36126">IClassFactory2::GetLicInfo</a> method.


## -struct-fields




### -field cbLicInfo

The size of the structure, in bytes.


### -field fRuntimeKeyAvail

Indicates whether this class factory allows the creation of its objects on an unlicensed machine through the use of a license key. If <b>TRUE</b>, <a href="https://msdn.microsoft.com/6c0211d2-1cdd-4d1a-a1fe-44c89b750af6">IClassFactory2::RequestLicKey</a> can be called to obtain the key. If <b>FALSE</b>, objects can be created only on a fully licensed machine.


### -field fLicVerified

Indicates whether a full machine license exists such that calls to <a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">IClassFactory::CreateInstance</a> and <a href="https://msdn.microsoft.com/6c0211d2-1cdd-4d1a-a1fe-44c89b750af6">IClassFactory2::RequestLicKey</a> will succeed. If <b>TRUE</b>, the full machine license exists. Thus, objects can be created freely. and a license key is available if <b>fRuntimeKeyAvail</b> is also <b>TRUE</b>. If <b>FALSE</b>, this class factory cannot create any instances of objects on this machine unless the proper license key is passed to <a href="https://msdn.microsoft.com/f33c7223-da7d-4582-9a23-7dc34be97a9f">IClassFactory2::CreateInstanceLic</a>.


## -see-also




<a href="https://msdn.microsoft.com/e55d1089-b1df-4de0-9a19-cbd255b36126">IClassFactory2::GetLicInfo</a>
 

 

