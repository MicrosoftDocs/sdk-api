---
UID: NF:pathcch.PathIsUNCEx
title: PathIsUNCEx function
author: windows-sdk-content
description: Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.This function differs from PathIsUNC in that it also allows you to extract the name of the server from the path.
old-location: shell\PathIsUNCEx.htm
old-project: shell
ms.assetid: 3b2a4158-63ec-49eb-a031-7493d02f2caa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PathIsUNCEx, PathIsUNCEx function [Windows Shell], pathcch/PathIsUNCEx, shell.PathIsUNCEx
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
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
 - PathIsUNCEx
product: Windows
targetos: Windows
req.lib: Pathcch.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# PathIsUNCEx function


## -description



Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.

This function differs from <a href="https://msdn.microsoft.com/53da5ba7-a2a4-45b2-90e0-ae006415933e">PathIsUNC</a> in that it also allows you to extract the name of the server from the path.




## -parameters




### -param pszPath [in]

A pointer to the path string.


### -param ppszServer [out, optional]

A pointer to a string that, when this function returns successfully, receives the server portion of the UNC path. This value can be <b>NULL</b> if you don't need this information.


## -returns



Returns <b>TRUE</b> if the string is a valid UNC path; otherwise, <b>FALSE</b>.



