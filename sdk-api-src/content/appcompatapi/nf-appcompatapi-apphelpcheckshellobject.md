---
UID: NF:appcompatapi.ApphelpCheckShellObject
title: ApphelpCheckShellObject function (appcompatapi.h)
description: Enables applications to detect bad extension objects and either block them from running or fix them.
helpviewer_keywords: ["ApphelpCheckShellObject","ApphelpCheckShellObject function [Windows API]","appcompatapi/ApphelpCheckShellObject","winprog.apphelpcheckshellobject"]
old-location: winprog\apphelpcheckshellobject.htm
tech.root: winprog
ms.assetid: e1e44cb1-ecfe-4a58-a29c-4a401f064a04
ms.date: 12/05/2018
ms.keywords: ApphelpCheckShellObject, ApphelpCheckShellObject function [Windows API], appcompatapi/ApphelpCheckShellObject, winprog.apphelpcheckshellobject
req.header: appcompatapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Apphelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ApphelpCheckShellObject
 - appcompatapi/ApphelpCheckShellObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-appcompat-apphelp-l1-1-2.dll
 - ext-ms-win-appcompat-apphelp-l1-1-1.dll
 - Apphelp.dll
 - Ext-MS-Win-AppCompat-AppHelp-L1-1-0.dll
api_name:
 - ApphelpCheckShellObject
---

# ApphelpCheckShellObject function


## -description

<p class="CCE_Message">[This function is available for use in the Windows Server 2003 and Windows XP operating systems. It may be altered or unavailable in the future.]

Enables applications to detect bad extension objects and either
            block them from running or fix them.

## -parameters

### -param ObjectCLSID [in]

The GUID of a register class.

### -param bShimIfNecessary [in]

This parameter is <b>TRUE</b> if a shim is needed; <b>FALSE</b> otherwise.

### -param pullFlags [out]

This parameter is filled with a 64-bit flag mask that can be used to turn on application modification flags in Explorer/IE. These are located in the application compatibility database.

## -returns

<b>FALSE</b> if the object should be blocked from instantiating; <b>TRUE</b> otherwise.

## -remarks

This is a helper function for Explorer and Internet Explorer that allows those applications to detect bad extension objects and either block them from running or fix them.


If the database indicates that a shim should be used to fix the extension
and <i>bShimIfNecessary</i> is <b>TRUE</b>, this function  loads Shimeng.dll and
applies the fix.

This function has no associated import library or header file; you must call it using the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions.