---
UID: NF:fwpmu.FwpmFreeMemory0
title: FwpmFreeMemory0 function (fwpmu.h)
description: Is used to release memory resources allocated by the Windows Filtering Platform (WFP) functions.
helpviewer_keywords: ["FwpmFreeMemory0","FwpmFreeMemory0 function [Filtering]","fwp.fwpmfreememory0_func","fwpmu/FwpmFreeMemory0"]
old-location: fwp\fwpmfreememory0_func.htm
tech.root: fwp
ms.assetid: ba9f8c1e-f75c-4bf0-b68b-e21a358575fc
ms.date: 12/05/2018
ms.keywords: FwpmFreeMemory0, FwpmFreeMemory0 function [Filtering], fwp.fwpmfreememory0_func, fwpmu/FwpmFreeMemory0
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmFreeMemory0
 - fwpmu/FwpmFreeMemory0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmFreeMemory0
---

# FwpmFreeMemory0 function


## -description

The <b>FwpmFreeMemory0</b> function is used to release memory resources allocated by the Windows Filtering Platform (WFP) functions.

## -parameters

### -param p [in, out]

Type: <b>void**</b>

Address of the pointer to be freed.

## -remarks

<b>FwpmFreeMemory0</b> is used to free memory returned by the various <b>Fwpm*</b> functions, such as <b>FwpmFilterGetByKey0</b>.

<b>Fwpm*</b> functions that return a HANDLE, such as <b>FwpmCalloutCreateEnumHandle0</b>, have specific functions to release memory.

If the caller passes a pointer that is not valid, the behavior is undefined.

<b>FwpmFreeMemory0</b> is a specific implementation of FwpmFreeMemory. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>



<a href="/windows/desktop/FWP/fwp-reference">Windows Filtering Platform  API Reference</a>