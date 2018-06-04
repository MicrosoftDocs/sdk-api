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

# _EVT_RPC_LOGIN structure


## -description


Contains the information used to connect to a remote computer.


## -struct-fields




### -field Server

The name of the remote computer to connect to.


### -field User

The user name to use to connect to the remote computer.


### -field Domain

The domain to which the user account belongs. Optional.


### -field Password

The password for the user account.


### -field Flags

The authentication method to use to authenticate the user when connecting to the remote computer. For possible authentication methods, see the <a href="https://msdn.microsoft.com/f3001756-7c2d-4a96-bbdf-e707debb5374">EVT_RPC_LOGIN_FLAGS</a> enumeration. 


## -remarks



You can set <b>User</b>, <b>Domain</b>, and <b>Password</b> to <b>NULL</b> to use the credentials of the current user.

If you set <b>Password</b>, consider using the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function to clear the password after calling <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a>.




## -see-also




<a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a>
 

 

