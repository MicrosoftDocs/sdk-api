---
UID: NF:shlobj_core.ILIsEmpty
title: ILIsEmpty function
author: windows-sdk-content
description: Verifies whether an ITEMIDLIST structure is empty.
old-location: shell\ILIsEmpty.htm
tech.root: shell
ms.assetid: bb727aad-9c4e-44dc-9c0c-4cbcbf3f9a78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILIsEmpty, ILIsEmpty function [Windows Shell], _shell_ILIsEmpty, shell.ILIsEmpty, shlobj_core/ILIsEmpty
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
 - ILIsEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILIsEmpty function


## -description


Verifies whether an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure is empty.


## -parameters




### -param pidl [in]

Type: <b>PCUID_RELATIVE</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be checked.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the <i>pidl</i> parameter is <b>NULL</b> or the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure pointed to by <i>pidl</i> is empty; otherwise <b>FALSE</b>.



