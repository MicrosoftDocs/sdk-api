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

# DPA_Clone function


## -description


<p class="CCE_Message">[<b>DPA_Clone</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Duplicates a dynamic pointer array (DPA).


## -parameters




### -param hdpa

TBD


### -param hdpaNew [in, out, optional]

Type: <b>HDPA</b>

When <b>NULL</b>, a new array is copied from <i>hdpaSource</i>. 

                    

This parameter can also contain an array created with <a href="https://msdn.microsoft.com/03bbfe08-69df-41da-85c8-41a96d9dac09">DPA_Create</a> or <a href="https://msdn.microsoft.com/a77ad74e-3bb5-414a-9cd7-db4b1c6e8116">DPA_CreateEx</a>. The data is overwritten but the original delta size and heap handle retained.


#### - hdpaSource [in]

Type: <b>const HDPA</b>

A handle to an existing DPA to copy.


## -returns



Type: <b>HDPA</b>

The handle to the new or altered DPA (<i>hdpaNew</i>) if successful; otherwise, <b>NULL</b>.




## -remarks



<b>DPA_Clone</b> is not exported by name or declared in a public header file. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 331 from ComCtl32.dll to obtain a function pointer.



