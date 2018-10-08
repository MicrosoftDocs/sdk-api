---
UID: NF:shlobj_core.ILCloneChild
title: ILCloneChild function
author: windows-sdk-content
description: Clones a child ITEMIDLIST structure.
old-location: shell\ILCloneChild.htm
tech.root: shell
ms.assetid: e82f0b34-3d7d-4da2-9eec-05842ede8300
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ILCloneChild, ILCloneChild function [Windows Shell], _shell_ILCloneChild, shell.ILCloneChild, shlobj_core/ILCloneChild
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
 - ILCloneChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILCloneChild function


## -description


Clones a child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to the child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be cloned.


## -returns



Type: <b>PCUITEMID_CHILD</b>

A pointer to a copy of the child <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure pointed to by <i>pidl</i>.




## -remarks



When you are finished with the cloned <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure, release it with <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a> to avoid memory leaks.



