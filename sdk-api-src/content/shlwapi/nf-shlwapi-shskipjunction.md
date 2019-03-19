---
UID: NF:shlwapi.SHSkipJunction
title: SHSkipJunction function (shlwapi.h)
author: windows-sdk-content
description: Checks a bind context to see if it is safe to bind to a particular component object.
old-location: shell\SHSkipJunction.htm
tech.root: shell
ms.assetid: 73af64a4-57eb-43db-91bb-75fe7134ad28
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SHSkipJunction, SHSkipJunction function [Windows Shell], _win32_SHSkipJunction, shell.SHSkipJunction, shlwapi/SHSkipJunction
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHSkipJunction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHSkipJunction function


## -description


Checks a bind context to see if it is safe to bind to a particular component object.


## -parameters




### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a> interface that specifies the bind context you want to check. This value can be <b>NULL</b>.


### -param pclsid [in]

Type: <b>const CLSID*</b>

A pointer to a variable that specifies the <b>CLSID</b> of the object being tested to see if it must be skipped. Typically, this is the CLSID of the object that <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> is about to create.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the object specified by <i>pclsid</i> must be skipped, or <b>FALSE</b> otherwise.




## -remarks



This function can be used to avoid infinite cycles in namespace binding. For example, a folder shortcut that refers to a folder above it in the namespace tree can produce an infinitely recursive loop.



