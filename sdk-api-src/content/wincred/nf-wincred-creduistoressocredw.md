---
UID: NF:wincred.CredUIStoreSSOCredW
title: CredUIStoreSSOCredW function
author: windows-sdk-content
description: The CredUIStoreSSOCredW function stores a single logon credential.
old-location: security\creduistoressocredw.htm
tech.root: secauthn
ms.assetid: 2c57c943-bcf7-405c-be0a-a3d1991f3004
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: CredUIStoreSSOCredW, CredUIStoreSSOCredW function [Security], security.creduistoressocredw, wincred/CredUIStoreSSOCredW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Credui.lib
req.dll: Credui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Credui.dll
 - Ext-MS-Win-security-credui-l1-1-1.dll
 - AnalogCredUI.dll
api_name:
 - CredUIStoreSSOCredW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

