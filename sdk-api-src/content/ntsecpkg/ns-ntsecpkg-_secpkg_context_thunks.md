---
UID: NS:ntsecpkg._SECPKG_CONTEXT_THUNKS
title: "_SECPKG_CONTEXT_THUNKS"
author: windows-sdk-content
description: The SECPKG_CONTEXT_THUNKS structure contains information about QueryContextAttributes (General) calls to be executed in LSA mode.This structure is used by the SpGetExtendedInformation and SpSetExtendedInformation functions.
old-location: security\secpkg_context_thunks.htm
old-project: secauthn
ms.assetid: 66604eaf-37f1-4c46-a62a-d8c821ad9039
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "*PSECPKG_CONTEXT_THUNKS, PSECPKG_CONTEXT_THUNKS, PSECPKG_CONTEXT_THUNKS structure pointer [Security], SECPKG_CONTEXT_THUNKS, SECPKG_CONTEXT_THUNKS structure [Security], _SECPKG_CONTEXT_THUNKS, _ssp_secpkg_context_thunks, ntsecpkg/PSECPKG_CONTEXT_THUNKS, ntsecpkg/SECPKG_CONTEXT_THUNKS, security.secpkg_context_thunks"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
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
tech.root: 
req.typenames: SECPKG_CONTEXT_THUNKS, *PSECPKG_CONTEXT_THUNKS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_CONTEXT_THUNKS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SECPKG_CONTEXT_THUNKS structure


## -description



			The <b>SECPKG_CONTEXT_THUNKS</b> structure contains information about 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> calls to be executed in LSA mode.

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field InfoLevelCount

The number of attributes specified by the <i>Levels</i> parameter.


### -field Levels

An array of one or more context attributes. For a complete list of valid values, see 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>.

