---
UID: NF:adshlp.AllocADsMem
title: AllocADsMem function (adshlp.h)
author: windows-sdk-content
description: Allocates a block of memory of the specified size.
old-location: adsi\allocadsmem.htm
tech.root: adsi
ms.assetid: df98a728-596b-4541-974a-5690e510ad9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllocADsMem, AllocADsMem function [ADSI], _ds_allocadsmem, adshlp/AllocADsMem, adsi.allocadsmem
ms.topic: function
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll; AdsLdpc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
 - AdsLdpc.dll
api_name:
 - AllocADsMem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AllocADsMem function


## -description


The <b>AllocADsMem</b> function allocates a block of memory of the specified size.


## -parameters




### -param cb [in]

Type: <b>DWORD</b>

Contains the size, in bytes, to be allocated.


## -returns



Type: <b>LPVOID</b>

When successful, the function returns a non-<b>NULL</b> pointer to the allocated memory. The caller must free this memory when it is no longer required by passing the returned pointer to <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>.

Returns <b>NULL</b> if not successful. Call  <a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a> to obtain extended error status. For more information about error code values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The memory block returned by <b>AllocADsMem</b> is initialized to zero.

For more information and a code example that shows how to use the <b>AllocADsMem</b> function, see <a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>
 

 

