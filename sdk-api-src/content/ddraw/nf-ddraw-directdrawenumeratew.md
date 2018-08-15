---
UID: NF:ddraw.DirectDrawEnumerateW
title: DirectDrawEnumerateW function
author: windows-sdk-content
description: This function is superseded by the DirectDrawEnumerateEx function.
old-location: directdraw\directdrawenumerate.htm
old-project: directdraw
ms.assetid: 1f994adb-79ff-4cc1-8769-0faeed893503
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DirectDrawEnumerate, DirectDrawEnumerate function [DirectDraw], DirectDrawEnumerateW, ddraw/DirectDrawEnumerate, ddraw/DirectDrawEnumerateW, directdraw.directdrawenumerate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddraw.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DirectDrawEnumerateW (Unicode) and DirectDrawEnumerate (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddraw.dll
api_name:
 - DirectDrawEnumerate
 - DirectDrawEnumerate
 - DirectDrawEnumerateW
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# DirectDrawEnumerateW function


## -description


This function is superseded by the <a href="https://msdn.microsoft.com/38edfaaf-2c19-4836-b662-343312220032">DirectDrawEnumerateEx</a> function.

The <b>DirectDrawEnumerate</b> function enumerates the primary DirectDraw display device and a nondisplay device (such as a 3-D accelerator that has no 2-D capabilities), if one is installed. The NULL entry always identifies the primary display device shared with the GDI.


## -parameters




### -param lpCallback [in]

Address of a <a href="https://msdn.microsoft.com/7F86FA67-C13B-49EE-8D17-9F54E5060A85">DDEnumCallback</a> function to be called with a description of each enumerated DirectDraw-enabled hardware abstraction layer (HAL).


### -param lpContext [in]

Address of an application-defined context to be passed to the enumeration callback function each time that it is called.


## -returns



If the function succeeds, the return value is <b>DD_OK</b>.

If it fails, the function returns <b>DDERR_INVALIDPARAMS</b>.




## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>DirectDrawEnumerate</b> function.



