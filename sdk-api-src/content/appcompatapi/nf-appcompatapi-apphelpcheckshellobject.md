---
UID: NF:appcompatapi.ApphelpCheckShellObject
title: ApphelpCheckShellObject function
author: windows-sdk-content
description: Enables applications to detect bad extension objects and either block them from running or fix them.
old-location: winprog\apphelpcheckshellobject.htm
tech.root: devnotes
ms.assetid: e1e44cb1-ecfe-4a58-a29c-4a401f064a04
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ApphelpCheckShellObject, ApphelpCheckShellObject function [Windows API], appcompatapi/ApphelpCheckShellObject, winprog.apphelpcheckshellobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Apphelp.dll
 - Ext-MS-Win-AppCompat-AppHelp-L1-1-0.dll
api_name:
 - ApphelpCheckShellObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

     This parameter is filled with a 64-bit flag mask that can be used to turn
            on   application modification flags in Explorer/IE. These are located in the application compatibility database.


## -returns



<b>FALSE</b> if the object should be blocked from instantiating; <b>TRUE</b> otherwise.




## -remarks



This is a helper function for Explorer and Internet Explorer that 
            allows those applications to detect bad extension objects and either
            block them from running or fix them.


            If the database indicates that a shim should be used to fix the extension
            and <i>bShimIfNecessary</i> is <b>TRUE</b>, this function  loads Shimeng.dll and
            applies the fix.

This function has no associated import library or header file; you must call it using the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions.



