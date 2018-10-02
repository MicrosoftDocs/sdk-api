---
UID: NF:shlobj_core.ILRemoveLastID
title: ILRemoveLastID function
author: windows-sdk-content
description: Removes the last SHITEMID structure from an ITEMIDLIST structure.
old-location: shell\ILRemoveLastID.htm
tech.root: Shell
ms.assetid: 144df03b-1adc-40c2-a864-3e16bdaf4915
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ILRemoveLastID, ILRemoveLastID function [Windows Shell], _win32_ILRemoveLastID, shell.ILRemoveLastID, shlobj_core/ILRemoveLastID
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
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
api_name:
 - ILRemoveLastID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILRemoveLastID function


## -description


Removes the last <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure from an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in, out, optional]

Type: <b>PUIDLIST_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be shortened. When the function returns, this variable points to the shortened structure.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.



