---
UID: NF:t2embapi.TTCharToUnicode
title: TTCharToUnicode function
author: windows-sdk-content
description: Converts an array of 8-bit character code values to 16-bit Unicode values.
old-location: gdi\ttchartounicode.htm
old-project: gdi
ms.assetid: b5ed9429-31fa-4f78-8fc3-aeb5cb1540d1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TTCharToUnicode, TTCharToUnicode function [Windows GDI], _win32_BytesToUnicode, gdi.ttchartounicode, t2embapi/TTCharToUnicode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: t2embapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
tech.root: 
req.typenames: SyncProviderConfiguration
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - T2embed.dll
api_name:
 - TTCharToUnicode
product: Windows
targetos: Windows
req.lib: T2embed.lib
req.dll: T2embed.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TTCharToUnicode function


## -description


Converts an array of 8-bit character code values to 16-bit Unicode values.


## -parameters




### -param hDC [in]

A device context handle.


### -param pucCharCodes [in]

A pointer to an array of 8-bit character codes to convert to 16-bit Unicode values. Must be set to a non-null value.


### -param ulCharCodeSize [in]

The size of an 8-bit character code array.


### -param pusShortCodes [out]

A pointer to an array that will be filled by this function with the Unicode equivalents of the 8-bit values in the <i>pucCharCodesarray</i>. This parameter must be set to a non-null value.


### -param ulShortCodeSize [in]

The size, in wide characters, of the character code array.


### -param ulFlags [in]

This parameter is currently unused.


## -returns



If successful, returns E_NONE.

Array *<i>pusShortCodes</i> is filled with 16-bit Unicode values that correspond to the 8-bit character codes in *<i>pusCharCodes</i>.<i>ulShortCodeSize</i> contains the size, in wide characters, of *<i>pusShortCodes</i>.

Otherwise, returns an error code described in <a href="https://msdn.microsoft.com/71effafe-55a9-40ed-81c7-07278eba32d3">Embedding Function Error Messages</a>.




## -remarks



This function may be useful to clients when creating a list of symbol characters to be subsetted.




## -see-also




<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a>



<a href="https://msdn.microsoft.com/b8c13444-86ab-479c-ac04-9b184d9eebf6">WideCharToMultiByte</a>
 

 

