---
UID: NF:shlobj_core.SHReplaceFromPropSheetExtArray
title: SHReplaceFromPropSheetExtArray function
author: windows-sdk-content
description: Requests each property sheet in a property sheet extension array to replace pages. Each page is allowed up to one replacement.
old-location: shell\SHReplaceFromPropSheetExtArray.htm
tech.root: shell
ms.assetid: a8bdde44-d668-46c4-9e58-7a45b775fe09
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SHReplaceFromPropSheetExtArray, SHReplaceFromPropSheetExtArray function [Windows Shell], _win32_SHReplaceFromPropSheetExtArray, shell.SHReplaceFromPropSheetExtArray, shlobj_core/SHReplaceFromPropSheetExtArray
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHReplaceFromPropSheetExtArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



