---
UID: NF:pathcch.PathCchStripToRoot
title: PathCchStripToRoot function
author: windows-sdk-content
description: Removes all file and directory elements in a path except for the root information.This function differs from PathStripToRoot in that it accepts paths with &#0034;\\&#0034;, &#0034;\\?\&#0034; and &#0034;\\?\UNC\&#0034; prefixes.
old-location: shell\PathCchStripToRoot.htm
tech.root: shell
ms.assetid: e0539478-8c64-4445-ab99-22f1df70afe8
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: PathCchStripToRoot, PathCchStripToRoot function [Windows Shell], pathcch/PathCchStripToRoot, shell.PathCchStripToRoot
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
 - PathCchStripToRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathCchStripToRoot function


## -description



Removes all file and directory elements in a path except for the root information.

This function differs from <a href="https://msdn.microsoft.com/ce9a1a40-2a03-44d2-80bc-0dc10654550b">PathStripToRoot</a> in that it accepts paths with "\\", "\\?\" and "\\?\UNC\" prefixes.


<div class="alert"><b>Note</b>  This function should be used in place of <a href="https://msdn.microsoft.com/ce9a1a40-2a03-44d2-80bc-0dc10654550b">PathStripToRoot</a> to prevent the possibility of a buffer overrun.</div><div> </div>

## -parameters




### -param pszPath [in, out]

A pointer to the path string. When this function returns successfully, this string contains only the root information taken from that path.


### -param cchPath [in]

The size of the buffer pointed to by <i>pszPath</i>, in characters.


## -returns



This function returns S_OK if the path was truncated, S_FALSE if the path was already just a root, or an HRESULT failure code.




## -remarks



Some examples of the effect of this function:
            
                

<table class="clsStd">
<tr>
<th>Initial string</th>
<th>Final string</th>
</tr>
<tr>
<td>"C:\path1\path2\file"</td>
<td>"C:\"</td>
</tr>
<tr>
<td>"\\path1\path2\path3"</td>
<td>"\\path1\path2"</td>
</tr>
<tr>
<td>"\path1"</td>
<td>"\"</td>
</tr>
</table>
 



