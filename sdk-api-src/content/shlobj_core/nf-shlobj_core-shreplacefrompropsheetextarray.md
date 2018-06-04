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

# SHReplaceFromPropSheetExtArray function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Requests each property sheet in a property sheet extension array to replace pages. Each page is allowed up to one replacement.


## -parameters




### -param hpsxa [in]

Type: <b>HPSXA</b>

A property sheet array handle (HPSXA) returned from a call to <a href="https://msdn.microsoft.com/88a72529-325d-431e-bc26-bddca787e62b">SHCreatePropSheetExtArray</a>.


### -param uPageID

Type: <b>UINT</b>

The ID of the page to replace.


### -param lpfnReplaceWith [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to an <a href="https://msdn.microsoft.com/37673813-89dc-4624-a58b-fe5f44df46c6">AddPropSheetPageProc</a> function used by the property sheet extension to add a page to a property sheet.


### -param lParam

Type: <b>LPARAM</b>

An application-defined value.


## -returns



Type: <b>UINT</b>

The number of replacements actually performed.



