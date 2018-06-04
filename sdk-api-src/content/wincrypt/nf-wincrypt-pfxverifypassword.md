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

# PFXVerifyPassword function


## -description


The <b>PFXVerifyPassword</b> function attempts to decode the outer layer of a BLOB as a Personal Information Exchange (PFX) packet and to decrypt it with the given password. No data from the BLOB is imported.

The PFX format is also known as the Public-Key Cryptography Standards #12 (PKCS #12) format.


## -parameters




### -param pPFX [in]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that the function will attempt to decode as a PFX packet.


### -param szPassword [in]

String password to be checked. For this function to succeed, this password must be exactly the same as the password used to encrypt the packet.

If you set this value to an empty string or <b>NULL</b>, this function typically attempts to decrypt the password embedded in the PFX BLOB by using the empty string or <b>NULL</b>.

However, beginning with Windows 8 and Windows Server 2012, if a <b>NULL</b> or empty password was specified when the PFX BLOB was created and the application also specified  that the password should be protected to an Active Directory (AD) principal, the Cryptography API (CAPI) randomly generates a password, encrypts it to the AD principal and embeds it in the PFX BLOB. The <b>PFXVerifyPassword</b> function will then try to use the specified AD principal (current user, computer, or AD group member) to decrypt the password. For more information about protecting PFX to an AD principal, see the <i>pvPara</i> parameter and the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag of the <a href="https://msdn.microsoft.com/e8bd54b1-946f-4c65-8a86-96f0dbec07ff">PFXExportCertStoreEx</a> function.

When you have finished using the password, clear the password from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param dwFlags [in]

Reserved for future use.


## -returns



The function return <b>TRUE</b> if the password appears correct; otherwise, it returns <b>FALSE</b>.



