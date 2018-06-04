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

# CredMarshalTargetInfo function


## -description


Serializes the specified target into an array of byte values.


## -parameters




### -param InTargetInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version of the <a href="https://msdn.microsoft.com/92180f2c-ef7c-4481-9b6f-19234c114afb">CREDENTIAL_TARGET_INFORMATION</a> structure that specifies the target to serialize.


### -param Buffer [out]

The serialized array of byte values that represents the target specified by the <i>InTargetInfo</i> parameter.


### -param BufferSize

The size, in bytes, of the <i>Buffer</i> array.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code that indicates the reason it failed.



