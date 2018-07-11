---
UID: NF:fwpmu.FwpmFreeMemory0
title: FwpmFreeMemory0 function
author: windows-sdk-content
description: Is used to release memory resources allocated by the Windows Filtering Platform (WFP) functions.
old-location: fwp\fwpmfreememory0_func.htm
old-project: fwp
ms.assetid: ba9f8c1e-f75c-4bf0-b68b-e21a358575fc
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FwpmFreeMemory0, FwpmFreeMemory0 function [Filtering], fwp.fwpmfreememory0_func, fwpmu/FwpmFreeMemory0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmFreeMemory0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmFreeMemory0 function


## -description


The <b>FwpmFreeMemory0</b> function is used to release memory resources allocated by the Windows Filtering Platform (WFP) functions.


## -parameters




### -param p [in, out]

Type: <b>void**</b>

Address of the pointer to be freed.


## -returns



This function does not return a value.




## -remarks



<b>FwpmFreeMemory0</b> is used to free memory returned by the various <b>Fwpm*</b> functions, such as <b>FwpmFilterGetByKey0</b>.

<b>Fwpm*</b> functions that return a HANDLE, such as <b>FwpmCalloutCreateEnumHandle0</b>, have specific functions to release memory.

If the caller passes a pointer that is not valid, the behavior is undefined.

<b>FwpmFreeMemory0</b> is a specific implementation of FwpmFreeMemory. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>



<a href="https://msdn.microsoft.com/e63db9e6-af26-4511-99fa-7d0b13d409d8">Windows Filtering Platform  API Reference</a>
 

 

