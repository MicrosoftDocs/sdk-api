---
UID: NS:ntsecpkg._SECPKG_EXTENDED_INFORMATION
title: "_SECPKG_EXTENDED_INFORMATION"
author: windows-sdk-content
description: The SECPKG_EXTENDED_INFORMATION structure is used to hold information about optional package capabilities.This structure is used by the SpGetExtendedInformation and SpSetExtendedInformation functions.
old-location: security\secpkg_extended_information.htm
old-project: secauthn
ms.assetid: 3d80dfc0-c35b-4d14-8196-02944c3db8d2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSECPKG_EXTENDED_INFORMATION, PSECPKG_EXTENDED_INFORMATION, PSECPKG_EXTENDED_INFORMATION structure pointer [Security], SECPKG_EXTENDED_INFORMATION, SECPKG_EXTENDED_INFORMATION structure [Security], _SECPKG_EXTENDED_INFORMATION, _ssp_secpkg_extended_information, ntsecpkg/PSECPKG_EXTENDED_INFORMATION, ntsecpkg/SECPKG_EXTENDED_INFORMATION, security.secpkg_extended_information"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SECPKG_EXTENDED_INFORMATION, *PSECPKG_EXTENDED_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_EXTENDED_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SECPKG_EXTENDED_INFORMATION structure


## -description


The <b>SECPKG_EXTENDED_INFORMATION</b> structure is used to hold information about optional package capabilities.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field Class

A value from the 
<a href="https://msdn.microsoft.com/52c24886-ae81-4ac8-97d5-d638016e82bf">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration which identifies the information in the structure.


### -field Info

Structure that contains the information.


### -field Info.GssInfo

A 
<a href="https://msdn.microsoft.com/a2df73ee-6c95-40d9-b1cb-9eaddb4100d6">SECPKG_GSS_INFO</a> structure that contains information used for GSS-compatible negotiations.


### -field Info.ContextThunks

A 
<a href="https://msdn.microsoft.com/66604eaf-37f1-4c46-a62a-d8c821ad9039">SECPKG_CONTEXT_THUNKS</a> structure that contains information about 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> calls to be executed in LSA mode.


### -field Info.MutualAuthLevel

A 
<a href="https://msdn.microsoft.com/f56cd322-8f82-43d7-a666-7067bf23b0a7">SECPKG_MUTUAL_AUTH_LEVEL</a> structure that contains the authentication level used by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


### -field Info.WowClientDll

A 
<a href="https://msdn.microsoft.com/AA48B271-E63F-4742-9776-6C85ED3A2BAB">SECPKG_WOW_CLIENT_DLL</a> structure that contains the path to the  WOW client's 32-bit version of the DLL used by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>. LSA operations are done by the 64-bit version. When the security context is handed back to the client,  the 32-bit WOW-aware version is loaded and hands it any information from the 64-bit version.


### -field Info.ExtraOids

A 
<a href="https://msdn.microsoft.com/188EB248-F056-40F4-8A27-6BEC75F14154">SECPKG_EXTRA_OIDS</a> structure that contains the extra object identifiers (OIDs) used by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


### -field Info.Nego2Info

A 
<a href="https://msdn.microsoft.com/8B093B74-DBF2-4DBD-9FDC-72FD6CC3CCA6">SECPKG_NEGO2_INFO</a> structure that contains the Nego2 information used by a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

