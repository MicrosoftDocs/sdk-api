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

# _WS_CAPI_ASYMMETRIC_SECURITY_KEY_HANDLE structure


## -description



The type for specifying asymmetric cryptographic keys as CAPI 1.0 key
handles.
            


When this structure is used in an API (such as 
with <a href="https://msdn.microsoft.com/1d82c6c3-2bcf-4883-aed7-1a163bbb2228">XML token creation</a> and subsequent
<a href="https://msdn.microsoft.com/5ca1e67a-11f5-44bb-afe8-c934837d711b">use of that XML
token</a> for a channel), the application is responsible for making
sure that the HCRYPTPROV remains valid as long as the key is in
use.  The application is also responsible for freeing the handle when
it is no longer in use.
            


This type is supported only on pre-Windows Vista platforms: for
Windows Vista and later, please use <a href="https://msdn.microsoft.com/843e8d93-3191-42e6-aa7b-d78b3b3370ec">WS_NCRYPT_ASYMMETRIC_SECURITY_KEY_HANDLE</a>.
            


## -struct-fields




### -field keyHandle


The base type from which this type and all other key handle types derive.
                


### -field provider


The cryptographic provider.
                


### -field keySpec


The key specification.
                

