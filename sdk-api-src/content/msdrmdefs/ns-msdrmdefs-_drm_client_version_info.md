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

# _DRM_CLIENT_VERSION_INFO structure


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRM_CLIENT_VERSION_INFO</b> structure receives information about the version of the Active Directory Rights Management Services (AD RMS) client and the hierarchy, such as Production or Pre-production. This structure is used by the <a href="https://msdn.microsoft.com/51f15900-4d7a-414e-ab2a-9120cd23a03b">DRMGetClientVersion</a> function.


## -struct-fields




### -field uStructVersion

Version of this structure, for backward compatibility. In C, this value should be initialized to <b>DRMCLIENTSTRUCTVERSION</b>.


### -field dwVersion

Array of type <b>DWORD</b> that receives the version number of the Active Directory Rights Management Services client software. The version number consists of the following parts.



#### dwVersion (0)

The client major version number.



#### dwVersion (1)

The client minor version number.



#### dwVersion (2)

The client build version number.



#### dwVersion (3)

The client private version number.


### -field wszHierarchy

Array of type <b>WCHAR</b> that receives the hierarchy information, such as Production or Pre-production.


### -field wszProductId

 


### -field wszProductDescription

Array of type <b>WCHAR</b> that receives the product description. This member is not currently filled by the <a href="https://msdn.microsoft.com/51f15900-4d7a-414e-ab2a-9120cd23a03b">DRMGetClientVersion</a> function.


#### - wszProductID

Array of type <b>WCHAR</b> that receives the product ID. This member  is not currently filled by the <a href="https://msdn.microsoft.com/51f15900-4d7a-414e-ab2a-9120cd23a03b">DRMGetClientVersion</a> function.


## -see-also




<a href="https://msdn.microsoft.com/06a0c6d2-108d-4c72-9ae6-8959304602c5">AD RMS Structures</a>



<a href="https://msdn.microsoft.com/51f15900-4d7a-414e-ab2a-9120cd23a03b">DRMGetClientVersion</a>
 

 

