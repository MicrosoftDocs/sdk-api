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

# SspiMarshalAuthIdentity function


## -description


Serializes the specified identity structure into a byte array.


## -parameters




### -param AuthIdentity [in]

The identity structure to serialize.


### -param AuthIdentityLength [out]

The length, in bytes, of the <i>AuthIdentityByteArray</i> array.


### -param AuthIdentityByteArray [out]

A pointer to an array of byte values that represents the identity specified by the <i>AuthIdentity</i> parameter.


## -returns




						If the function succeeds, it returns <b>SEC_E_OK</b>.

If the function fails, it returns a nonzero error code.



