---
UID: NF:adshlp.AllocADsStr
title: AllocADsStr function
author: windows-sdk-content
description: Allocates memory for and copies a specified string.
old-location: adsi\allocadsstr.htm
old-project: ADSI
ms.assetid: 1e2b6d42-a879-4a53-a2ce-0e841f6b8543
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: AllocADsStr, AllocADsStr function [ADSI], _ds_allocadsstr, adshlp/AllocADsStr, adsi.allocadsstr
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - AllocADsStr
product: Windows
targetos: Windows
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
---

# AllocADsStr function


## -description


The <b>AllocADsStr</b> function allocates memory for and copies a specified string.


## -parameters




### -param pStr [in]

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string to be copied.


## -returns



Type: <b>LPWSTR</b>

When successful, the function returns a non-<b>NULL</b> pointer to the allocated memory. The string in <i>pStr</i> is copied to this buffer and null-terminated. The caller must  free this memory when it is no longer required by passing the returned pointer to <a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a>.

Returns <b>NULL</b> if not successful. Call  <a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a> to obtain the extended error status. For more information about error code values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



For more information and a code example that shows how to use the <b>AllocADsStr</b> function, see <a href="https://msdn.microsoft.com/805d45dc-8da4-4c15-a6d1-8967a4da9c24">ReallocADsStr</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">ADsGetLastError</a>



<a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a>



<a href="https://msdn.microsoft.com/805d45dc-8da4-4c15-a6d1-8967a4da9c24">ReallocADsStr</a>
 

 

