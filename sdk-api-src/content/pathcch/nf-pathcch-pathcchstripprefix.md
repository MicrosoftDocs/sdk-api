---
UID: NF:pathcch.PathCchStripPrefix
title: PathCchStripPrefix function
author: windows-sdk-content
description: Removes the &#0034;\\?\&#0034; prefix, if present, from a file path.
old-location: shell\PathCchStripPrefix.htm
tech.root: Shell
ms.assetid: 2e50b23e-2725-4200-bd5e-845ff3458026
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: PathCchStripPrefix, PathCchStripPrefix function [Windows Shell], pathcch/PathCchStripPrefix, shell.PathCchStripPrefix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Pathcch.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - pathcch.lib
 - API-MS-Win-Core-Path-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PathCchStripPrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathCchStripPrefix function


## -description



Removes the "\\?\" prefix, if present, from a file path.




## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, the same path string will have had the prefix removed, if the prefix was present. If no prefix was present, the string will be unchanged.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the prefix was removed, S_FALSE if the path did not have a prefix to remove, or an HRESULT failure code.



