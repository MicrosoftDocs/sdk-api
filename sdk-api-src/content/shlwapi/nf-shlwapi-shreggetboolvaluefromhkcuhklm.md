---
UID: NF:shlwapi.SHRegGetBoolValueFromHKCUHKLM
title: SHRegGetBoolValueFromHKCUHKLM function (shlwapi.h)
description: Evaluates a registry key value and returns a boolean value that reflects whether the value exists and the expected state matches the actual state.
helpviewer_keywords: ["SHRegGetBoolValueFromHKCUHKLM","SHRegGetBoolValueFromHKCUHKLM function [Windows Shell]","_shell_SHRegGetBoolValueFromHKCUHKLM","shell.SHRegGetBoolValueFromHKCUHKLM","shlwapi/SHRegGetBoolValueFromHKCUHKLM"]
old-location: shell\SHRegGetBoolValueFromHKCUHKLM.htm
tech.root: shell
ms.assetid: 05239aef-a6cf-426f-919e-08b70baee3f8
ms.date: 12/05/2018
ms.keywords: SHRegGetBoolValueFromHKCUHKLM, SHRegGetBoolValueFromHKCUHKLM function [Windows Shell], _shell_SHRegGetBoolValueFromHKCUHKLM, shell.SHRegGetBoolValueFromHKCUHKLM, shlwapi/SHRegGetBoolValueFromHKCUHKLM
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHRegGetBoolValueFromHKCUHKLM
 - shlwapi/SHRegGetBoolValueFromHKCUHKLM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-shlwapi-ie-l1-1-0.dll
 - shlwapi.dll
api_name:
 - SHRegGetBoolValueFromHKCUHKLM
---

# SHRegGetBoolValueFromHKCUHKLM function


## -description

<p class="CCE_Message">[This function is no longer supported.]

Evaluates a registry key value and returns a boolean value that reflects whether the value exists and the expected state matches the actual state. This function will first check HKEY_CURRENT_USER for the requested information in the specified subkey. If the information does not exist under the HKEY_CURRENT_USER subtree it will check the HKEY_LOCAL_MACHINE subtree for the same information.

## -parameters

### -param pszKey

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the path to the key to be checked.

### -param pszValue [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated Unicode string that specifies the value to be evaluated.

### -param fDefault [in]

Type: <b>BOOL</b>

The expected state of the evaluation, as defined by the calling function.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the evaluation matches the <i>fDefault</i> value; otherwise, <b>FALSE</b>.

