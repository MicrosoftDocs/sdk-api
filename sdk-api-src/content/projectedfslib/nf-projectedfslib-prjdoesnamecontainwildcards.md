---
UID: NF:projectedfslib.PrjDoesNameContainWildCards
title: PrjDoesNameContainWildCards function
author: windows-sdk-content
description: Determines whether a name contains wildcard characters.
old-location: projfs\prjdoesnamecontainwildcards.htm
tech.root: ProjFS
ms.assetid: AE1896D4-0DFB-477F-ADD8-C6C14DAD27CD
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: PrjDoesNameContainWildCards, PrjDoesNameContainWildCards function, ProjFS.prjdoesnamecontainwildcards, projectedfslib/PrjDoesNameContainWildCards
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - projectedfslib.h
api_name:
 - PrjDoesNameContainWildCards
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PrjDoesNameContainWildCards function


## -description


Determines whether a name contains wildcard characters.


## -parameters




### -param fileName [in]

A null-terminated Unicode string to check for wildcard characters.


## -returns



True if fileName contains wildcards, False otherwise.



