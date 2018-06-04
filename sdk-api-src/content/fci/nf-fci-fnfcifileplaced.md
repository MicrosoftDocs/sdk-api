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

# FNFCIFILEPLACED macro


## -description


The <b>FNFCIFILEPLACED</b> macro provides the declaration for the application-defined callback function to notify when a file is placed in the cabinet.


## -parameters




### -param fn

TBD






#### - cbFile

The length of the file in bytes.


#### - fContinuation

A boolean value that is <b>TRUE</b> if the data added is a segment of a continued file.


#### - pccab

Pointer to the <a href="https://msdn.microsoft.com/e25cb72b-4c96-40e9-9fd5-2920e4a01d3a">CCAB</a> structure containing the parameters of the cabinet on which the file has been stored.


#### - pszFile [in]

The name of the file in the cabinet.


#### - pv

Pointer to an application-defined value.

