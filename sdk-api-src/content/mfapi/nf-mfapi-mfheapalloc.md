---
UID: NF:mfapi.MFHeapAlloc
title: MFHeapAlloc function
author: windows-sdk-content
description: Allocates a block of memory.
old-location: mf\mfheapalloc.htm
old-project: medfound
ms.assetid: 3ad97cbf-4065-4807-ad6a-68e84a3601d4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 3ad97cbf-4065-4807-ad6a-68e84a3601d4, MFHeapAlloc, MFHeapAlloc function [Media Foundation], mf.mfheapalloc, mfapi/MFHeapAlloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFHeapAlloc
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFHeapAlloc function


## -description



Allocates a block of memory.




## -parameters




### -param nSize [in]

Number of bytes to allocate.


### -param dwFlags [in]

Zero or more flags. For a list of valid flags, see <b>HeapAlloc</b> in the Windows SDK documentation.


### -param pszFile [in]


            Reserved. Set to <b>NULL</b>.
          


### -param line [in]


            Reserved. Set to zero.
          


### -param eat [in]


            Reserved. Set to <b>eAllocationTypeIgnore</b>.
          


## -returns



If the function succeeds, it returns a pointer to the allocated memory block. If the function fails, it returns <b>NULL</b>.




## -remarks



In the current version of Media Foundation, this function is equivalent to calling the <b>HeapAlloc</b> function and specifying the heap of the calling process.

To free the allocated memory, call <a href="https://msdn.microsoft.com/c4a03a20-5398-4fe0-9a1f-3bc162c624cd">MFHeapFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

