---
UID: NF:shlobj_core.ILSkip
title: ILSkip function
author: windows-sdk-content
description: Skips a given number of bytes in a constant, unaligned, relative ITEMIDLIST structure.
old-location: shell\ILSkip_PCUIDLIST_RELATIVE_UINT.htm
tech.root: shell
ms.assetid: 0ed0409a-eab3-49b6-bd8d-06ad38ac2f8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILSkip, ILSkip function [Windows Shell], ILSkip(PCUIDLIST_RELATIVE,UINT), _shell_ILSkip_PCUIDLIST_RELATIVE_UINT, shell.ILSkip_PCUIDLIST_RELATIVE_UINT, shlobj_core/ILSkip
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
 - ILSkip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILSkip function


## -description


Skips a given number of bytes in a constant, unaligned, relative <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant, unaligned, relative PIDL in which bytes are to be skipped.


### -param cb

Type: <b>UINT</b>

The number of bytes to skip.


## -returns



Type: <b>PCUIDLIST_RELATIVE</b>

When this function returns, if <i>pidl</i> and <i>cb</i> are valid, contains a constant pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure that results after the skip. Otherwise, the value is meaningless.




## -remarks



For use where STRICT_TYPED_ITEMIDS is defined.



