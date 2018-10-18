---
UID: NF:shellapi.SHTestTokenMembership
title: SHTestTokenMembership function
author: windows-sdk-content
description: Uses CheckTokenMembership to test whether the given token is a member of the local group with the specified RID.
old-location: shell\SHTestTokenMembership.htm
tech.root: shell
ms.assetid: ac2d591a-f431-4da7-aa9f-0476634ec9cf
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: SHTestTokenMembership, SHTestTokenMembership function [Windows Shell], _win32_SHTestTokenMembership, shell.SHTestTokenMembership, shellapi/SHTestTokenMembership
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHTestTokenMembership
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHTestTokenMembership function


## -description


Uses <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a> to test whether the given token is a member of the local group with the specified RID.


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



This function wraps <a href="https://msdn.microsoft.com/c254a167-c4e7-4b84-9be3-6862761309f8">CheckTokenMembership</a> and only checks local groups.



