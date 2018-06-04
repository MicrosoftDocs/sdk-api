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

# CredUIStoreSSOCredW function


## -description


The <b>CredUIStoreSSOCredW</b> function stores a single logon credential.


## -parameters




### -param pszRealm [in]

Pointer to a <b>null</b>-terminated string that specifies the realm. If this parameter is <b>NULL</b>, the default realm is used.


### -param pszUsername [in]

Pointer to a <b>null</b>-terminated string that specifies the user's name.


### -param pszPassword [in]

Pointer to a <b>null</b>-terminated string that specifies the user's password. When you have finished using the password, clear the password from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param bPersist [in]

Boolean value that specifies whether the credentials are persisted. If this value is <b>TRUE</b>, the credentials are persisted. If this value is <b>FALSE</b>, the credentials are not persisted.


## -returns



The return value is a <b>DWORD</b>. A return value of ERROR_SUCCESS indicates the function was successful.




## -see-also




<a href="https://msdn.microsoft.com/875be45d-ad33-4a51-80ad-8217ca0446dc">CredUIReadSSOCredW</a>
 

 

