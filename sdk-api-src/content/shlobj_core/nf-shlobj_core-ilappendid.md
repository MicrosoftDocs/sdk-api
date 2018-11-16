---
UID: NF:shlobj_core.ILAppendID
title: ILAppendID function
author: windows-sdk-content
description: Appends or prepends an SHITEMID structure to an ITEMIDLIST structure.
old-location: shell\ILAppendID.htm
tech.root: shell
ms.assetid: d1bb5993-fe23-42d4-a2c5-8e54e6e37d09
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ILAppendID, ILAppendID function [Windows Shell], _win32_ILAppendID, shell.ILAppendID, shlobj_core/ILAppendID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Windows.Storage.dll
api_name:
 - ILAppendID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ILAppendID
: 
---

# ILAppendID function


## -description


Appends or prepends an <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in, optional]

Type: <b>PIDLIST_RELATIVE</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure. When the function returns, the <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure specified by <i>pmkid</i> is appended or prepended.


### -param pmkid [in]

Type: <b>LPSHITEMID</b>

A pointer to a <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure to be appended or prepended to <i>pidl</i>.


### -param fAppend

Type: <b>BOOL</b>

Value that is set to <b>TRUE</b> to append <i>pmkid</i> to <i>pidl</i>. Set this value to <b>FALSE</b> to prepend <i>pmkid</i> to <i>pidl</i>.


## -returns



Type: <b>PIDLIST_RELATIVE</b>

Returns the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure specified by <i>pidl</i>, with <i>pmkid</i> appended or prepended. Returns <b>NULL</b> on failure.



