---
UID: NF:propvarutil.VariantToFileTime
title: VariantToFileTime function
author: windows-sdk-content
description: Extracts a FILETIME structure from a variant structure.
old-location: properties\VariantToFileTime.htm
old-project: properties
ms.assetid: e3094bd1-e641-43d8-8bc5-926c8d5a6ebe
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PSTF_LOCAL, PSTF_UTC, VariantToFileTime, VariantToFileTime function [Windows Properties], _shell_VariantToFileTime, properties.VariantToFileTime, propvarutil/VariantToFileTime, shell.VariantToFileTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToFileTime
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToFileTime function


## -description


Extracts a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure from a variant structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param stfOut [in]

Type: <b>PSTIME_FLAGS</b>

Specifies one of the following time flags:



#### PSTF_UTC (0)

Indicates coordinated universal time.



#### PSTF_LOCAL (1)

Indicates local time.


### -param pftOut [out]

Type: <b>FILETIME*</b>

Pointer to the extracted <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<i>stfOut</i> flags override any property description flags.



