---
UID: NF:adshlp.FreeADsMem
title: FreeADsMem function
author: windows-sdk-content
description: Frees the memory allocated by AllocADsMem or ReallocADsMem.
old-location: adsi\freeadsmem.htm
old-project: ADSI
ms.assetid: e43f050a-5b96-406e-87ed-88a39ea747da
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: FreeADsMem, FreeADsMem function [ADSI], _ds_freeadsmem, adshlp/FreeADsMem, adsi.freeadsmem
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
 - AdsLdpc.dll
api_name:
 - FreeADsMem
product: Windows
targetos: Windows
req.lib: Activeds.lib
req.dll: Activeds.dll; AdsLdpc.dll
req.irql: 
---

# FreeADsMem function


## -description


The <b>FreeADsMem</b> function frees the memory allocated by  <a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a> or <a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>.


## -parameters




### -param pMem [in]

Type: <b>LPVOID</b>

Pointer to the memory to be freed. This memory must have been allocated with the <a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a> or <a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a> function.


## -returns



Type: <b>BOOL</b>

The function returns <b>TRUE</b> if successful, otherwise it returns <b>FALSE</b>.




## -remarks



Do not use this  function to free memory allocated with the <a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a> or <a href="https://msdn.microsoft.com/805d45dc-8da4-4c15-a6d1-8967a4da9c24">ReallocADsStr</a> function. Use the  <a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a> function to free memory allocated with these functions.

For more information and  a code example that shows how to use the <b>FreeADsMem</b> function, see <a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>.




## -see-also




<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/df98a728-596b-4541-974a-5690e510ad9f">AllocADsMem</a>



<a href="https://msdn.microsoft.com/1e2b6d42-a879-4a53-a2ce-0e841f6b8543">AllocADsStr</a>



<a href="https://msdn.microsoft.com/9c8eaac2-1fb4-47f9-8f60-6896073012aa">FreeADsStr</a>



<a href="https://msdn.microsoft.com/471b8ae7-d3b6-4dd9-aa00-6e1d3ab278a9">ReallocADsMem</a>



<a href="https://msdn.microsoft.com/805d45dc-8da4-4c15-a6d1-8967a4da9c24">ReallocADsStr</a>
 

 

