---
UID: NF:shellapi.SHTestTokenMembership
title: SHTestTokenMembership function (shellapi.h)
description: Uses CheckTokenMembership to test whether the given token is a member of the local group with the specified RID.
helpviewer_keywords: ["SHTestTokenMembership","SHTestTokenMembership function [Windows Shell]","_win32_SHTestTokenMembership","shell.SHTestTokenMembership","shellapi/SHTestTokenMembership"]
old-location: shell\SHTestTokenMembership.htm
tech.root: shell
ms.assetid: ac2d591a-f431-4da7-aa9f-0476634ec9cf
ms.date: 12/05/2018
ms.keywords: SHTestTokenMembership, SHTestTokenMembership function [Windows Shell], _win32_SHTestTokenMembership, shell.SHTestTokenMembership, shellapi/SHTestTokenMembership
req.header: shellapi.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHTestTokenMembership
 - shellapi/SHTestTokenMembership
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHTestTokenMembership
---

# SHTestTokenMembership function


## -description

Uses <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a> to test whether the given token is a member of the local group with the specified RID.

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

This function wraps <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership">CheckTokenMembership</a> and only checks local groups.