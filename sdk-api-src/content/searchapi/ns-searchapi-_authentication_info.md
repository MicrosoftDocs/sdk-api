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

# _AUTHENTICATION_INFO structure


## -description


Describes security authentication information for content access.


## -struct-fields




### -field dwSize

Type: <b>DWORD</b>

Size of the structure, in bytes.
                


### -field atAuthenticationType

Type: <b><a href="https://msdn.microsoft.com/430a8631-6ee9-460c-a05c-d930001e1974">AUTH_TYPE</a></b>

Flag to describe the type of authentication. For a list of possible values, see the <a href="https://msdn.microsoft.com/430a8631-6ee9-460c-a05c-d930001e1974">AUTH_TYPE</a> enumerated type.


### -field pcwszUser

Type: <b>LPCWSTR</b>


                Pointer to a null-terminated Unicode string containing the user name.
                


### -field pcwszPassword

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string containing the password for <b> pcwszUser</b>.
                

