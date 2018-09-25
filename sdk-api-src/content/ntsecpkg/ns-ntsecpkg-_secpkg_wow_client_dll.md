---
UID: NS:ntsecpkg._SECPKG_WOW_CLIENT_DLL
title: "_SECPKG_WOW_CLIENT_DLL"
author: windows-sdk-content
description: Contains the path to the WOW-aware 32-bit DLL.
old-location: security\secpkg_wow_client_dll.htm
tech.root: secauthn
ms.assetid: AA48B271-E63F-4742-9776-6C85ED3A2BAB
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PSECPKG_WOW_CLIENT_DLL, PSECPKG_WOW_CLIENT_DLL, PSECPKG_WOW_CLIENT_DLL structure pointer [Security], SECPKG_WOW_CLIENT_DLL, SECPKG_WOW_CLIENT_DLL structure [Security], _SECPKG_WOW_CLIENT_DLL, ntsecpkg/PSECPKG_WOW_CLIENT_DLL, ntsecpkg/SECPKG_WOW_CLIENT_DLL, security.secpkg_wow_client_dll"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_WOW_CLIENT_DLL
product: Windows
targetos: Windows
req.typenames: SECPKG_WOW_CLIENT_DLL, *PSECPKG_WOW_CLIENT_DLL
req.redist: 
---

# _SECPKG_WOW_CLIENT_DLL structure


## -description


The <b>SECPKG_WOW_CLIENT_DLL</b> structure contains the path to the WOW-aware 32-bit DLL.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field WowClientDllPath

A <a href="https://msdn.microsoft.com/4E03761C-8199-4D9F-B9DA-8941F0CC6700">SECURITY_STRING</a> that contain the path to the WOW-aware client 32-bit library.

