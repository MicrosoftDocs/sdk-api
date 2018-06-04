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

# SHTestTokenMembership function


## -description


Uses <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a> to test whether the given token is a member of the local group with the specified RID.


## -parameters




### -param hToken [in, optional]

Type: <b>HANDLE</b>

A handle to the token. This value can be <b>NULL</b>.


### -param ulRID

Type: <b>ULONG</b>

The RID of the local group for which membership is tested.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> on success, <b>FALSE</b> on failure.




## -remarks



This function wraps <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a> and only checks local groups.



