---
UID: NF:pathcch.PathCchRenameExtension
title: PathCchRenameExtension function
author: windows-driver-content
description: Replaces a file name's extension at the end of a path string with a new extension.
old-location: shell\PathCchRenameExtension.htm
old-project: shell
ms.assetid: 79cd9499-03b7-4482-abd3-a42edd1b2b67
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PathCchRenameExtension, PathCchRenameExtension function [Windows Shell], pathcch/PathCchRenameExtension, shell.PathCchRenameExtension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: pathcch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	pathcch.lib
-	API-MS-Win-Core-Path-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PathCchRenameExtension
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PathCchRenameExtension function


## -description



Replaces a file name's extension at the end of a path string with a new extension. If the path string does not end with an extension, the new extension is added.

This function differs from <a href="https://msdn.microsoft.com/3d94f67c-e3ee-4b64-b0b9-8f771423bdc5">PathRenameExtension</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/3d94f67c-e3ee-4b64-b0b9-8f771423bdc5">PathRenameExtension</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, this value points to the same string, but with the renamed or added extension.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


### -param pszExt [in]

A pointer to the new extension string. The leading '.' character is optional. In the case of an empty string (""), any existing extension in the path string is removed.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



