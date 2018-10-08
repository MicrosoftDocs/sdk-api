---
UID: NF:shlwapi.SHGetAssocKeys
title: SHGetAssocKeys function
author: windows-sdk-content
description: Retrieves an array of class subkeys associated with an IQueryAssociations object.
old-location: shell\shgetassockeys.htm
tech.root: shell
ms.assetid: 0DCB7E41-5986-40CA-A68D-EC6688EB42C0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SHGetAssocKeys, SHGetAssocKeys function [Windows Shell], shell.shgetassockeys, shlwapi/SHGetAssocKeys
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHGetAssocKeys
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHGetAssocKeys function


## -description


Retrieves an array of class subkeys associated with an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> object.


## -parameters




### -param pqa [in]

A <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface pointer to the object you're interested in.


### -param rgKeys [out]

A pointer to an array of <b>HKEY</b> elements that, when this function returns successfully, receives the retrived class subkeys.


### -param cKeys

The number of elements in the <i>rgKeys</i> array. If you are interested in only the primary class subkey, set this value to 1.


## -returns



The number of subkeys inserted into the array.



