---
UID: NF:mfapi.MFHeapAlloc
title: MFHeapAlloc function (mfapi.h)
author: windows-sdk-content
description: Allocates a block of memory.
old-location: mf\mfheapalloc.htm
tech.root: medfound
ms.assetid: 3ad97cbf-4065-4807-ad6a-68e84a3601d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3ad97cbf-4065-4807-ad6a-68e84a3601d4, MFHeapAlloc, MFHeapAlloc function [Media Foundation], mf.mfheapalloc, mfapi/MFHeapAlloc
ms.topic: function
f1_keywords: 
 - "mfapi/MFHeapAlloc"
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFHeapAlloc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

To free the allocated memory, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfheapfree">MFHeapFree</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

