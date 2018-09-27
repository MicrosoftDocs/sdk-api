---
UID: NF:fci.FNFCIFILEPLACED
title: FNFCIFILEPLACED macro
author: windows-sdk-content
description: The FNFCIFILEPLACED macro provides the declaration for the application-defined callback function to notify when a file is placed in the cabinet.
old-location: winprog\fnfcifileplaced.htm
tech.root: devnotes
ms.assetid: f8a1bcfc-8a13-49cf-a3e7-caec6c6421b0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FNFCIFILEPLACED, FNFCIFILEPLACED macro [Windows API], fci/FNFCIFILEPLACED, winprog.fnfcifileplaced
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: fci.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIFILEPLACED
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCIFILEPLACED macro


## -description


The <b>FNFCIFILEPLACED</b> macro provides the declaration for the application-defined callback function to notify when a file is placed in the cabinet.


## -parameters




### -param fn

Pointer to the <a href="https://msdn.microsoft.com/e25cb72b-4c96-40e9-9fd5-2920e4a01d3a">CCAB</a> structure containing the parameters of the cabinet on which the file has been stored.


#### - cbFile

The length of the file in bytes.


#### - fContinuation

A boolean value that is <b>TRUE</b> if the data added is a segment of a continued file.


#### - pszFile [in]

The name of the file in the cabinet.


#### - pv

Pointer to an application-defined value.

