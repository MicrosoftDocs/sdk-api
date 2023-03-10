---
UID: NF:powrprof.PowerImportPowerScheme
title: PowerImportPowerScheme function (powrprof.h)
description: Imports a power scheme from a file.
helpviewer_keywords: ["PowerImportPowerScheme","PowerImportPowerScheme function","base.powerimportpowerscheme","powrprof/PowerImportPowerScheme"]
old-location: base\powerimportpowerscheme.htm
tech.root: base
ms.assetid: 84ba8cb6-13ad-459b-b154-c495aaeb67f3
ms.date: 12/05/2018
ms.keywords: PowerImportPowerScheme, PowerImportPowerScheme function, base.powerimportpowerscheme, powrprof/PowerImportPowerScheme
req.header: powrprof.h
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerImportPowerScheme
 - powrprof/PowerImportPowerScheme
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - PowerImportPowerScheme
---

# PowerImportPowerScheme function


## -description

Imports a power scheme from a file.

## -parameters

### -param RootPowerKey [in]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param ImportFileNamePath [in]

The path to a power scheme backup file created by <b>PowerCfg.Exe /Export</b>.

### -param DestinationSchemeGuid [in, out]

A pointer to a pointer to a <b>GUID</b>. If the pointer contains 
      <b>NULL</b>, the function allocates memory for a new 
      <b>GUID</b> and puts the address of this memory in the pointer. The caller can free this 
      memory using <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> (zero) if the call was successful, and a nonzero value if 
      the call failed.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>