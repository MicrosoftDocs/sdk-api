---
UID: NF:shlobj_core.ILCloneFull
title: ILCloneFull function
author: windows-sdk-content
description: Clones a full, or absolute, ITEMIDLIST structure.
old-location: shell\ILCloneFull.htm
tech.root: shell
ms.assetid: 60af0eb7-306a-45f8-b5ce-eb6451f380d5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ILCloneFull, ILCloneFull function [Windows Shell], _shell_ILCloneFull, shell.ILCloneFull, shlobj_core/ILCloneFull
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
 - ILCloneFull
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILCloneFull function


## -description


Clones a full, or absolute, <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_ABSOLUTE</b>

A pointer to the full, or absolute, <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure to be cloned.


## -returns



Type: <b>PIDLIST_ABSOLUTE</b>

A pointer to a copy of the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure pointed to by <i>pidl</i>.




## -remarks



When you are finished with the cloned <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure, release it with <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a> to avoid memory leaks.



