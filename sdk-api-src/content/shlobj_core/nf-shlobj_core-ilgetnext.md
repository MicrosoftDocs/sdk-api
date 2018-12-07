---
UID: NF:shlobj_core.ILGetNext
title: ILGetNext function
author: windows-sdk-content
description: Retrieves the next SHITEMID structure in an ITEMIDLIST structure.
old-location: shell\ILGetNext.htm
tech.root: shell
ms.assetid: 0b58cc30-fe1a-487c-8f24-f1de54f7730f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILGetNext, ILGetNext function [Windows Shell], _win32_ILGetNext, shell.ILGetNext, shlobj_core/ILGetNext
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
 - ILGetNext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILGetNext function


## -description


Retrieves the next <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in, optional]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a particular <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in a larger <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -returns



Type: <b>PUIDLIST_RELATIVE</b>

Returns a pointer to the <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure that follows the one specified by <i>pidl</i>. Returns <b>NULL</b> if <i>pidl</i> points to the last <b>SHITEMID</b> structure.



