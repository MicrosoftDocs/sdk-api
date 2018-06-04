---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PathIsNetworkPathW function


## -description


Determines whether a path string represents a network resource.


## -parameters




### -param pszPath [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string of maximum length MAX_PATH that contains the path.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string represents a network resource, or <b>FALSE</b> otherwise.




## -remarks



<b>PathIsNetworkPath</b> interprets the following two types of paths as network paths.

<ul>
<li>Paths that begin with two backslash characters (\\) are interpreted as Universal Naming Convention (UNC) paths.</li>
<li>Paths that begin with a letter followed by a colon (:) are interpreted as a mounted network drive. However, <b>PathIsNetworkPath</b> cannot recognize a network drive mapped to a drive letter through the Microsoft MS-DOS SUBST command or the <a href="https://msdn.microsoft.com/924b1456-b2c5-4d52-aacf-6172608c73ea">DefineDosDevice</a> function.</li>
</ul>
<div class="alert"><b>Note</b>  The function does not verify that the specified network resource exists, is currently accessible, or that the user has sufficient permissions to access it.</div>
<div> </div>


