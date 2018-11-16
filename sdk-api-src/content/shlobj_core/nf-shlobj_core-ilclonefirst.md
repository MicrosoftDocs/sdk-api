---
UID: NF:shlobj_core.ILCloneFirst
title: ILCloneFirst function
author: windows-sdk-content
description: Clones the first SHITEMID structure in an ITEMIDLIST structure.
old-location: shell\ILCloneFirst.htm
tech.root: shell
ms.assetid: 931df0c7-6acb-4c49-aa2b-464255e97347
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ILCloneFirst, ILCloneFirst function [Windows Shell], _win32_ILCloneFirst, shell.ILCloneFirst, shlobj_core/ILCloneFirst
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
 - ILCloneFirst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ILCloneFirst
: 
---

# ILCloneFirst function


## -description


Clones the first <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure in an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that you want to clone.


## -returns



Type: <b>PITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that contains the first <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a> structure from the <b>ITEMIDLIST</b> structure specified by <i>pidl</i>. Returns <b>NULL</b> on failure.




## -see-also




<a href="https://msdn.microsoft.com/90689575-3308-4817-ae8c-380fa5f55c88">ILClone</a>
 

 

