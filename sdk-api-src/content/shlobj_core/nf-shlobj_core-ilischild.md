---
UID: NF:shlobj_core.ILIsChild
title: ILIsChild function
author: windows-sdk-content
description: Verifies whether a pointer to an item identifier list (PIDL) is a child PIDL, which is a PIDL with exactly one SHITEMID.
old-location: shell\ILIsChild.htm
tech.root: Shell
ms.assetid: e799fbcf-8254-457a-9d1b-6202dea190c1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ILIsChild, ILIsChild function [Windows Shell], _shell_ILIsChild, shell.ILIsChild, shlobj_core/ILIsChild
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - ILIsChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILIsChild function


## -description


Verifies whether a pointer to an item identifier list (PIDL) is a child PIDL, which is a PIDL with exactly one <a href="https://msdn.microsoft.com/794c8425-2319-4339-881c-c5083ab05638">SHITEMID</a>.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant, unaligned, relative PIDL that is being checked.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the given PIDL is a child PIDL; otherwise, <b>FALSE</b>.




## -remarks



This function does not guarantee that the PIDL is non-NULL or non-empty.

For use where STRICT_TYPED_ITEMIDS is defined.



